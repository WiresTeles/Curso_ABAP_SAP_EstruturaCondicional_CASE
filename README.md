# Curso_ABAP_SAP_EstruturaCondicional_CASE
WiresTeles/Curso_ABAP_SAP_EstruturaCondicional_CASE
REPORT ZCURSO_008.

SELECTION-SCREEN BEGIN OF BLOCK b1.
  PARAMETER p_cat TYPE c. "CHAR
SELECTION-SCREEN END OF BLOCK b1.

START-OF-SELECTION.
DATA ld_descricao TYPE string.

  CASE p_cat.
    WHEN 'A'.
      ld_descricao = 'MOTO'.
    WHEN 'B'.
      ld_descricao ='CARRO'.
    WHEN 'C'.
      ld_descricao =  'VEÍCULOS DE CARGA'.
    WHEN 'D'.
      ld_descricao ='TRANSPORTE DE PASSAGEIRO'.
    WHEN 'E'.
      ld_descricao ='TRANSPORTE DE CAMINHÕES'.
    WHEN OTHERS.
      ld_descricao ='CATEGORIA INVÁLIDA'.
  ENDCASE.

  WRITE ld_descricao.
