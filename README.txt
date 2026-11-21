#if defined _RIO_RISE_MAPA
    #endinput
#endif
#define _RIO_RISE_MAPA

// ======================================
// RIO RISE RP - MAPA CLASSICO
// SA-MP 0.3.7 / MOBILE
// ======================================

#define RR_COR_AZUL       0x00AFFFFF
#define RR_COR_VERDE      0x00FF00FF
#define RR_COR_ROXO       0xAA44FFFF
#define RR_COR_VERMELHO   0xFF3333FF
#define RR_COR_BRANCO     0xFFFFFFFF

forward RR_CriarMapa();
forward RR_CriarIcones(playerid);

public RR_CriarMapa()
{
    // CENTRO DA CIDADE
    Create3DTextLabel(
        "{00AFFF}CENTRO DA CIDADE",
        RR_COR_AZUL,
        1481.0, -1730.0, 15.0,
        100.0, 0, 0
    );

    // PREFEITURA
    Create3DTextLabel(
        "{FFFFFF}PREFEITURA\n{00AFFF}RIO RISE RP",
        RR_COR_BRANCO,
        1470.0, -1740.0, 15.0,
        60.0, 0, 0
    );

    // HOSPITAL
    Create3DTextLabel(
        "{FF3333}HOSPITAL CENTRAL",
        RR_COR_VERMELHO,
        1530.0, -1700.0, 15.0,
        60.0, 0, 0
    );

    // POLICIA
    Create3DTextLabel(
        "{00AFFF}DELEGACIA DE POLICIA",
        RR_COR_AZUL,
        1430.0, -1600.0, 15.0,
        60.0, 0, 0
    );

    // FAVELA
    Create3DTextLabel(
        "{FF3333}FAVELA DO RIO",
        RR_COR_VERMELHO,
        2200.0, -1400.0, 15.0,
        100.0, 0, 0
    );

    // ORGANIZACAO VERDE
    Create3DTextLabel(
        "{00FF00}ORGANIZACAO VERDE",
        RR_COR_VERDE,
        2500.0, -1650.0, 15.0,
        60.0, 0, 0
    );

    // ORGANIZACAO ROXA
    Create3DTextLabel(
        "{AA44FF}ORGANIZACAO ROXA",
        RR_COR_ROXO,
        2600.0, -1800.0, 15.0,
        60.0, 0, 0
    );

    // CONCESSIONARIA
    Create3DTextLabel(
        "{FFFFFF}CONCESSIONARIA",
        RR_COR_BRANCO,
        1100.0, -1350.0, 15.0,
        60.0, 0, 0
    );

    // BANCO
    Create3DTextLabel(
        "{00FF00}BANCO CENTRAL",
        RR_COR_VERDE,
        1450.0, -1020.0, 15.0,
        60.0, 0, 0
    );

    // MANSOES
    Create3DTextLabel(
        "{FFFFFF}AREA DAS MANSOES",
        RR_COR_BRANCO,
        1000.0, -900.0, 15.0,
        80.0, 0, 0
    );

    print("[RIO RISE] Pontos do mapa carregados.");
    return 1;
}

public RR_CriarIcones(playerid)
{
    // PREFEITURA
    SetPlayerMapIcon(
        playerid, 0,
        1470.0, -1740.0, 15.0,
        0, RR_COR_AZUL, MAPICON_GLOBAL
    );

    // HOSPITAL
    SetPlayerMapIcon(
        playerid, 1,
        1530.0, -1700.0, 15.0,
        22, RR_COR_VERMELHO, MAPICON_GLOBAL
    );

    // POLICIA
    SetPlayerMapIcon(
        playerid, 2,
        1430.0, -1600.0, 15.0,
        30, RR_COR_AZUL, MAPICON_GLOBAL
    );

    // FAVELA
    SetPlayerMapIcon(
        playerid, 3,
        2200.0, -1400.0, 15.0,
        0, RR_COR_VERMELHO, MAPICON_GLOBAL
    );

    // CONCESSIONARIA
    SetPlayerMapIcon(
        playerid, 4,
        1100.0, -1350.0, 15.0,
        55, RR_COR_BRANCO, MAPICON_GLOBAL
    );

    // BANCO
    SetPlayerMapIcon(
        playerid, 5,
        1450.0, -1020.0, 15.0,
        52, RR_COR_VERDE, MAPICON_GLOBAL
    );

    return 1;
}
#include <a_samp>
#include "rio_rise_mapa.inc"
RR_CriarMapa();
RR_CriarIcones(playerid);
