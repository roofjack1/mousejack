                                      1 ;--------------------------------------------------------
                                      2 ; File Created by SDCC : free open source ANSI-C Compiler
                                      3 ; Version 3.5.0 #9253 (Feb 24 2016) (Mac OS X x86_64)
                                      4 ; This file was generated Wed Feb 24 11:52:24 2016
                                      5 ;--------------------------------------------------------
                                      6 	.module main
                                      7 	.optsdcc -mmcs51 --model-large
                                      8 	
                                      9 ;--------------------------------------------------------
                                     10 ; Public variables in this module
                                     11 ;--------------------------------------------------------
                                     12 	.globl _main
                                     13 	.globl _spi_write
                                     14 	.globl _init_usb
                                     15 	.globl _RFRDY
                                     16 	.globl _rfcsn
                                     17 	.globl _rfce
                                     18 	.globl _ien1
                                     19 	.globl _ien0
                                     20 	.globl _RFDAT
                                     21 	.globl _P0DIR
                                     22 	.globl _P0
                                     23 	.globl _usbcon
                                     24 	.globl _rfcon
                                     25 	.globl _rfctl
                                     26 	.globl _setupbuf
                                     27 	.globl _out1buf
                                     28 	.globl _in1buf
                                     29 	.globl _in0buf
                                     30 ;--------------------------------------------------------
                                     31 ; special function registers
                                     32 ;--------------------------------------------------------
                                     33 	.area RSEG    (ABS,DATA)
      000000                         34 	.org 0x0000
                           0000E6    35 _rfctl	=	0x00e6
                           000090    36 _rfcon	=	0x0090
                           0000A0    37 _usbcon	=	0x00a0
                           000080    38 _P0	=	0x0080
                           000094    39 _P0DIR	=	0x0094
                           0000E5    40 _RFDAT	=	0x00e5
                           0000A8    41 _ien0	=	0x00a8
                           0000B8    42 _ien1	=	0x00b8
                                     43 ;--------------------------------------------------------
                                     44 ; special function bits
                                     45 ;--------------------------------------------------------
                                     46 	.area RSEG    (ABS,DATA)
      000000                         47 	.org 0x0000
                           000090    48 _rfce	=	0x0090
                           000091    49 _rfcsn	=	0x0091
                           0000C0    50 _RFRDY	=	0x00c0
                                     51 ;--------------------------------------------------------
                                     52 ; overlayable register banks
                                     53 ;--------------------------------------------------------
                                     54 	.area REG_BANK_0	(REL,OVR,DATA)
      000000                         55 	.ds 8
                                     56 ;--------------------------------------------------------
                                     57 ; internal ram data
                                     58 ;--------------------------------------------------------
                                     59 	.area DSEG    (DATA)
                                     60 ;--------------------------------------------------------
                                     61 ; overlayable items in internal ram 
                                     62 ;--------------------------------------------------------
                                     63 ;--------------------------------------------------------
                                     64 ; Stack segment in internal ram 
                                     65 ;--------------------------------------------------------
                                     66 	.area	SSEG
      000022                         67 __start__stack:
      000022                         68 	.ds	1
                                     69 
                                     70 ;--------------------------------------------------------
                                     71 ; indirectly addressable internal ram data
                                     72 ;--------------------------------------------------------
                                     73 	.area ISEG    (DATA)
                                     74 ;--------------------------------------------------------
                                     75 ; absolute internal ram data
                                     76 ;--------------------------------------------------------
                                     77 	.area IABS    (ABS,DATA)
                                     78 	.area IABS    (ABS,DATA)
                                     79 ;--------------------------------------------------------
                                     80 ; bit data
                                     81 ;--------------------------------------------------------
                                     82 	.area BSEG    (BIT)
      000000                         83 _configured:
      000000                         84 	.ds 1
                                     85 ;--------------------------------------------------------
                                     86 ; paged external ram data
                                     87 ;--------------------------------------------------------
                                     88 	.area PSEG    (PAG,XDATA)
                                     89 ;--------------------------------------------------------
                                     90 ; external ram data
                                     91 ;--------------------------------------------------------
                                     92 	.area XSEG    (XDATA)
                           00C700    93 _in0buf	=	0xc700
                           00C680    94 _in1buf	=	0xc680
                           00C640    95 _out1buf	=	0xc640
                           00C7E8    96 _setupbuf	=	0xc7e8
      008000                         97 _in_pm:
      008000                         98 	.ds 1
      008001                         99 _pm_prefix_length:
      008001                        100 	.ds 2
      008003                        101 _pm_prefix:
      008003                        102 	.ds 5
                                    103 ;--------------------------------------------------------
                                    104 ; absolute external ram data
                                    105 ;--------------------------------------------------------
                                    106 	.area XABS    (ABS,XDATA)
                                    107 ;--------------------------------------------------------
                                    108 ; external initialized ram data
                                    109 ;--------------------------------------------------------
                                    110 	.area XISEG   (XDATA)
      00806E                        111 _bootloader:
      00806E                        112 	.ds 2
      008070                        113 _promiscuous_address:
      008070                        114 	.ds 2
                                    115 	.area HOME    (CODE)
                                    116 	.area GSINIT0 (CODE)
                                    117 	.area GSINIT1 (CODE)
                                    118 	.area GSINIT2 (CODE)
                                    119 	.area GSINIT3 (CODE)
                                    120 	.area GSINIT4 (CODE)
                                    121 	.area GSINIT5 (CODE)
                                    122 	.area GSINIT  (CODE)
                                    123 	.area GSFINAL (CODE)
                                    124 	.area CSEG    (CODE)
                                    125 ;--------------------------------------------------------
                                    126 ; interrupt vector 
                                    127 ;--------------------------------------------------------
                                    128 	.area HOME    (CODE)
      000000                        129 __interrupt_vect:
      000000 02 00 6B         [24]  130 	ljmp	__sdcc_gsinit_startup
      000003 32               [24]  131 	reti
      000004                        132 	.ds	7
      00000B 32               [24]  133 	reti
      00000C                        134 	.ds	7
      000013 32               [24]  135 	reti
      000014                        136 	.ds	7
      00001B 32               [24]  137 	reti
      00001C                        138 	.ds	7
      000023 32               [24]  139 	reti
      000024                        140 	.ds	7
      00002B 32               [24]  141 	reti
      00002C                        142 	.ds	7
      000033 32               [24]  143 	reti
      000034                        144 	.ds	7
      00003B 32               [24]  145 	reti
      00003C                        146 	.ds	7
      000043 32               [24]  147 	reti
      000044                        148 	.ds	7
      00004B 32               [24]  149 	reti
      00004C                        150 	.ds	7
      000053 32               [24]  151 	reti
      000054                        152 	.ds	7
      00005B 32               [24]  153 	reti
      00005C                        154 	.ds	7
      000063 02 01 79         [24]  155 	ljmp	_usb_irq
                                    156 ;--------------------------------------------------------
                                    157 ; global & static initialisations
                                    158 ;--------------------------------------------------------
                                    159 	.area HOME    (CODE)
                                    160 	.area GSINIT  (CODE)
                                    161 	.area GSFINAL (CODE)
                                    162 	.area GSINIT  (CODE)
                                    163 	.globl __sdcc_gsinit_startup
                                    164 	.globl __sdcc_program_startup
                                    165 	.globl __start__stack
                                    166 	.globl __mcs51_genXINIT
                                    167 	.globl __mcs51_genXRAMCLEAR
                                    168 	.globl __mcs51_genRAMCLEAR
                                    169 	.area GSFINAL (CODE)
      0000C4 02 00 66         [24]  170 	ljmp	__sdcc_program_startup
                                    171 ;--------------------------------------------------------
                                    172 ; Home
                                    173 ;--------------------------------------------------------
                                    174 	.area HOME    (CODE)
                                    175 	.area HOME    (CODE)
      000066                        176 __sdcc_program_startup:
      000066 02 00 C7         [24]  177 	ljmp	_main
                                    178 ;	return from main will return to caller
                                    179 ;--------------------------------------------------------
                                    180 ; code
                                    181 ;--------------------------------------------------------
                                    182 	.area CSEG    (CODE)
                                    183 ;------------------------------------------------------------
                                    184 ;Allocation info for local variables in function 'main'
                                    185 ;------------------------------------------------------------
                                    186 ;	src/main.c:23: void main()
                                    187 ;	-----------------------------------------
                                    188 ;	 function main
                                    189 ;	-----------------------------------------
      0000C7                        190 _main:
                           000007   191 	ar7 = 0x07
                           000006   192 	ar6 = 0x06
                           000005   193 	ar5 = 0x05
                           000004   194 	ar4 = 0x04
                           000003   195 	ar3 = 0x03
                           000002   196 	ar2 = 0x02
                           000001   197 	ar1 = 0x01
                           000000   198 	ar0 = 0x00
                                    199 ;	src/main.c:25: rfcon = 0x06; // enable RF clock
      0000C7 75 90 06         [24]  200 	mov	_rfcon,#0x06
                                    201 ;	src/main.c:26: rfctl = 0x10; // enable SPI
      0000CA 75 E6 10         [24]  202 	mov	_rfctl,#0x10
                                    203 ;	src/main.c:27: ien0 = 0x80;  // enable interrupts
      0000CD 75 A8 80         [24]  204 	mov	_ien0,#0x80
                                    205 ;	src/main.c:30: init_usb();
      0000D0 12 00 FB         [24]  206 	lcall	_init_usb
                                    207 ;	src/main.c:33: flush_rx();
      0000D3 90 80 24         [24]  208 	mov	dptr,#_spi_write_PARM_2
      0000D6 E4               [12]  209 	clr	a
      0000D7 F0               [24]  210 	movx	@dptr,a
      0000D8 A3               [24]  211 	inc	dptr
      0000D9 F0               [24]  212 	movx	@dptr,a
      0000DA A3               [24]  213 	inc	dptr
      0000DB F0               [24]  214 	movx	@dptr,a
      0000DC 90 80 27         [24]  215 	mov	dptr,#_spi_write_PARM_3
      0000DF F0               [24]  216 	movx	@dptr,a
      0000E0 75 82 E2         [24]  217 	mov	dpl,#0xE2
      0000E3 12 06 5E         [24]  218 	lcall	_spi_write
                                    219 ;	src/main.c:34: flush_tx();
      0000E6 90 80 24         [24]  220 	mov	dptr,#_spi_write_PARM_2
      0000E9 E4               [12]  221 	clr	a
      0000EA F0               [24]  222 	movx	@dptr,a
      0000EB A3               [24]  223 	inc	dptr
      0000EC F0               [24]  224 	movx	@dptr,a
      0000ED A3               [24]  225 	inc	dptr
      0000EE F0               [24]  226 	movx	@dptr,a
      0000EF 90 80 27         [24]  227 	mov	dptr,#_spi_write_PARM_3
      0000F2 F0               [24]  228 	movx	@dptr,a
      0000F3 75 82 E1         [24]  229 	mov	dpl,#0xE1
      0000F6 12 06 5E         [24]  230 	lcall	_spi_write
                                    231 ;	src/main.c:37: while(1);
      0000F9                        232 00102$:
      0000F9 80 FE            [24]  233 	sjmp	00102$
                                    234 	.area CSEG    (CODE)
                                    235 	.area CONST   (CODE)
                                    236 	.area XINIT   (CODE)
      000FD3                        237 __xinit__bootloader:
      000FD3 00 78                  238 	.byte #0x00,#0x78
      000FD5                        239 __xinit__promiscuous_address:
      000FD5 AA                     240 	.db #0xAA	; 170
      000FD6 00                     241 	.db #0x00	; 0
                                    242 	.area CABS    (ABS,CODE)
