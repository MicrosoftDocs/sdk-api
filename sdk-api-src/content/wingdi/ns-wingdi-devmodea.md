---
UID: NS:wingdi._devicemodeA
title: DEVMODEA (wingdi.h)
description: The DEVMODE data structure contains information about the initialization and environment of a printer or a display device.
helpviewer_keywords: ["*LPDEVMODEA","*NPDEVMODEA","*PDEVMODEA","DEVMODE","DEVMODE structure [Windows GDI]","DEVMODEA","DMBIN_AUTO","DMBIN_CASSETTE","DMBIN_ENVELOPE","DMBIN_ENVMANUAL","DMBIN_FIRST","DMBIN_FORMSOURCE","DMBIN_LARGECAPACITY","DMBIN_LARGEFMT","DMBIN_LAST","DMBIN_LOWER","DMBIN_MANUAL","DMBIN_MIDDLE","DMBIN_ONLYONE","DMBIN_SMALLFMT","DMBIN_TRACTOR","DMBIN_UPPER","DMRES_DRAFT","DMRES_HIGH","DMRES_LOW","DMRES_MEDIUM","LPDEVMODE","LPDEVMODE structure pointer [Windows GDI]","PDEVMODE","PDEVMODE structure pointer [Windows GDI]","_DEVMODEA","_DEVMODEW","_win32_DEVMODE_str","gdi.devmode","wingdi/DEVMODE","wingdi/LPDEVMODE","wingdi/PDEVMODE","wingdi/_DEVMODEA","wingdi/_DEVMODEW"]
old-location: gdi\devmode.htm
tech.root: xps
ms.assetid: 85741025-9393-42ab-8a6d-27f1ae2c0f1b
ms.date: 12/05/2018
ms.keywords: '*LPDEVMODEA, *NPDEVMODEA, *PDEVMODEA, DEVMODE, DEVMODE structure [Windows GDI], DEVMODEA, DMBIN_AUTO, DMBIN_CASSETTE, DMBIN_ENVELOPE, DMBIN_ENVMANUAL, DMBIN_FIRST, DMBIN_FORMSOURCE, DMBIN_LARGECAPACITY, DMBIN_LARGEFMT, DMBIN_LAST, DMBIN_LOWER, DMBIN_MANUAL, DMBIN_MIDDLE, DMBIN_ONLYONE, DMBIN_SMALLFMT, DMBIN_TRACTOR, DMBIN_UPPER, DMRES_DRAFT, DMRES_HIGH, DMRES_LOW, DMRES_MEDIUM, LPDEVMODE, LPDEVMODE structure pointer [Windows GDI], PDEVMODE, PDEVMODE structure pointer [Windows GDI], _DEVMODEA, _DEVMODEW, _win32_DEVMODE_str, gdi.devmode, wingdi/DEVMODE, wingdi/LPDEVMODE, wingdi/PDEVMODE, wingdi/_DEVMODEA, wingdi/_DEVMODEW'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: _DEVMODEW (Unicode) and _DEVMODEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DEVMODEA, *PDEVMODEA, *NPDEVMODEA, *LPDEVMODEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _devicemodeA
 - wingdi/_devicemodeA
 - PDEVMODEA
 - wingdi/PDEVMODEA
 - DEVMODEA
 - wingdi/DEVMODEA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - DEVMODE
 - _DEVMODEA
 - _DEVMODEW
---

# DEVMODEA structure


## -description

The <b>DEVMODE</b> data structure contains information about the initialization and environment of a printer or a display device.

## -struct-fields

### -field dmDeviceName

A zero-terminated character array that specifies the "friendly" name of the printer or display; for example, "PCL/HP LaserJet" in the case of PCL/HP LaserJet. This string is unique among device drivers. Note that this name may be truncated to fit in the <b>dmDeviceName</b> array.

### -field dmSpecVersion

The version number of the initialization data specification on which the structure is based. To ensure the correct version is used for any operating system, use DM_SPECVERSION.

### -field dmDriverVersion

The driver version number assigned by the driver developer.

### -field dmSize

Specifies the size, in bytes, of the <b>DEVMODE</b> structure, not including any private driver-specific data that might follow the structure's public members. Set this member to <code>sizeof (DEVMODE)</code> to indicate the version of the <b>DEVMODE</b> structure being used.

### -field dmDriverExtra

Contains the number of bytes of private driver-data that follow this structure. If a device driver does not use device-specific information, set this member to zero.

### -field dmFields

Specifies whether certain members of the <b>DEVMODE</b> structure have been initialized. If a member is initialized, its corresponding bit is set, otherwise the bit is clear. A driver supports only those <b>DEVMODE</b> members that are appropriate for the printer or display technology.

The following values are defined, and are listed here with the corresponding structure members.

<table>
<tr>
<th>Value</th>
<th>Structure member</th>
</tr>
<tr>
<td>DM_ORIENTATION</td>
<td><b>dmOrientation</b></td>
</tr>
<tr>
<td>DM_PAPERSIZE</td>
<td><b>dmPaperSize</b></td>
</tr>
<tr>
<td>DM_PAPERLENGTH</td>
<td><b>dmPaperLength</b></td>
</tr>
<tr>
<td>DM_PAPERWIDTH</td>
<td><b>dmPaperWidth</b></td>
</tr>
<tr>
<td>DM_SCALE</td>
<td><b>dmScale</b></td>
</tr>
<tr>
<td>DM_COPIES</td>
<td><b>dmCopies</b></td>
</tr>
<tr>
<td>DM_DEFAULTSOURCE</td>
<td><b>dmDefaultSource</b></td>
</tr>
<tr>
<td>DM_PRINTQUALITY</td>
<td><b>dmPrintQuality</b></td>
</tr>
<tr>
<td>DM_POSITION</td>
<td><b>dmPosition</b></td>
</tr>
<tr>
<td>DM_DISPLAYORIENTATION</td>
<td><b>dmDisplayOrientation</b></td>
</tr>
<tr>
<td>DM_DISPLAYFIXEDOUTPUT</td>
<td><b>dmDisplayFixedOutput</b></td>
</tr>
<tr>
<td>DM_COLOR</td>
<td><b>dmColor</b></td>
</tr>
<tr>
<td>DM_DUPLEX</td>
<td><b>dmDuplex</b></td>
</tr>
<tr>
<td>DM_YRESOLUTION</td>
<td><b>dmYResolution</b></td>
</tr>
<tr>
<td>DM_TTOPTION</td>
<td><b>dmTTOption</b></td>
</tr>
<tr>
<td>DM_COLLATE</td>
<td><b>dmCollate</b></td>
</tr>
<tr>
<td>DM_FORMNAME</td>
<td><b>dmFormName</b></td>
</tr>
<tr>
<td>DM_LOGPIXELS</td>
<td><b>dmLogPixels</b></td>
</tr>
<tr>
<td>DM_BITSPERPEL</td>
<td><b>dmBitsPerPel</b></td>
</tr>
<tr>
<td>DM_PELSWIDTH</td>
<td><b>dmPelsWidth</b></td>
</tr>
<tr>
<td>DM_PELSHEIGHT</td>
<td><b>dmPelsHeight</b></td>
</tr>
<tr>
<td>DM_DISPLAYFLAGS</td>
<td><b>dmDisplayFlags</b></td>
</tr>
<tr>
<td>DM_NUP</td>
<td><b>dmNup</b></td>
</tr>
<tr>
<td>DM_DISPLAYFREQUENCY</td>
<td><b>dmDisplayFrequency</b></td>
</tr>
<tr>
<td>DM_ICMMETHOD</td>
<td><b>dmICMMethod</b></td>
</tr>
<tr>
<td>DM_ICMINTENT</td>
<td><b>dmICMIntent</b></td>
</tr>
<tr>
<td>DM_MEDIATYPE</td>
<td><b>dmMediaType</b></td>
</tr>
<tr>
<td>DM_DITHERTYPE</td>
<td><b>dmDitherType</b></td>
</tr>
<tr>
<td>DM_PANNINGWIDTH</td>
<td><b>dmPanningWidth</b></td>
</tr>
<tr>
<td>DM_PANNINGHEIGHT</td>
<td><b>dmPanningHeight</b></td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmOrientation

For printer devices only, selects the orientation of the paper. This member can be either DMORIENT_PORTRAIT (1) or DMORIENT_LANDSCAPE (2).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmPaperSize

For printer devices only, selects the size of the paper to print on. This member can be set to zero if the length and width of the paper are both set by the <b>dmPaperLength</b> and <b>dmPaperWidth</b> members. Otherwise, the <b>dmPaperSize</b> member can be set to a device specific value greater than or equal to DMPAPER_USER or to one of the following predefined values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMPAPER_LETTER</td>
<td>Letter, 8 1/2- by 11-inches</td>
</tr>
<tr>
<td>DMPAPER_LEGAL</td>
<td>Legal, 8 1/2- by 14-inches</td>
</tr>
<tr>
<td>DMPAPER_9X11</td>
<td>9- by 11-inch sheet</td>
</tr>
<tr>
<td>DMPAPER_10X11</td>
<td>10- by 11-inch sheet</td>
</tr>
<tr>
<td>DMPAPER_10X14</td>
<td>10- by 14-inch sheet</td>
</tr>
<tr>
<td>DMPAPER_15X11</td>
<td>15- by 11-inch sheet</td>
</tr>
<tr>
<td>DMPAPER_11X17</td>
<td>11- by 17-inch sheet</td>
</tr>
<tr>
<td>DMPAPER_12X11</td>
<td> 12- by 11-inch sheet
                    </td>
</tr>
<tr>
<td>DMPAPER_A2</td>
<td>A2 sheet, 420 x 594-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A3</td>
<td>A3 sheet, 297- by 420-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A3_EXTRA</td>
<td>A3 Extra 322 x 445-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A3_EXTRA_TRAVERSE</td>
<td>A3 Extra Transverse 322 x 445-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A3_ROTATED</td>
<td> A3 rotated sheet, 420- by 297-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_A3_TRAVERSE</td>
<td>A3 Transverse 297 x 420-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A4</td>
<td>A4 sheet, 210- by 297-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A4_EXTRA</td>
<td>A4 sheet, 9.27 x 12.69 inches</td>
</tr>
<tr>
<td>DMPAPER_A4_PLUS</td>
<td>A4 Plus 210 x 330-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A4_ROTATED</td>
<td> A4 rotated sheet, 297- by 210-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_A4SMALL</td>
<td>A4 small sheet, 210- by 297-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A4_TRANSVERSE</td>
<td>A4 Transverse 210 x 297 millimeters</td>
</tr>
<tr>
<td>DMPAPER_A5</td>
<td>A5 sheet, 148- by 210-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A5_EXTRA</td>
<td>A5 Extra 174 x 235-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A5_ROTATED</td>
<td> A5 rotated sheet, 210- by 148-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_A5_TRANSVERSE</td>
<td>A5 Transverse 148 x 210-millimeters</td>
</tr>
<tr>
<td>DMPAPER_A6</td>
<td> A6 sheet, 105- by 148-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_A6_ROTATED</td>
<td> A6 rotated sheet, 148- by 105-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_A_PLUS</td>
<td>SuperA/A4 227 x 356 -millimeters</td>
</tr>
<tr>
<td>DMPAPER_B4</td>
<td>B4 sheet, 250- by 354-millimeters</td>
</tr>
<tr>
<td>DMPAPER_B4_JIS_ROTATED</td>
<td> B4 (JIS) rotated sheet, 364- by 257-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_B5</td>
<td>B5 sheet, 182- by 257-millimeter paper</td>
</tr>
<tr>
<td>DMPAPER_B5_EXTRA</td>
<td>B5 (ISO) Extra 201 x 276-millimeters</td>
</tr>
<tr>
<td>DMPAPER_B5_JIS_ROTATED</td>
<td> B5 (JIS) rotated sheet, 257- by 182-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_B6_JIS</td>
<td> B6 (JIS) sheet, 128- by 182-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_B6_JIS_ROTATED</td>
<td> B6 (JIS) rotated sheet, 182- by 128-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_B_PLUS</td>
<td>SuperB/A3 305 x 487-millimeters</td>
</tr>
<tr>
<td>DMPAPER_CSHEET</td>
<td>C Sheet, 17- by 22-inches</td>
</tr>
<tr>
<td>DMPAPER_DBL_JAPANESE_POSTCARD</td>
<td> Double Japanese Postcard, 200- by 148-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_DBL_JAPANESE_POSTCARD_ROTATED</td>
<td> Double Japanese Postcard Rotated, 148- by 200-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_DSHEET</td>
<td>D Sheet, 22- by 34-inches</td>
</tr>
<tr>
<td>DMPAPER_ENV_9</td>
<td>#9 Envelope, 3 7/8- by 8 7/8-inches</td>
</tr>
<tr>
<td>DMPAPER_ENV_10</td>
<td>#10 Envelope, 4 1/8- by 9 1/2-inches</td>
</tr>
<tr>
<td>DMPAPER_ENV_11</td>
<td>#11 Envelope, 4 1/2- by 10 3/8-inches</td>
</tr>
<tr>
<td>DMPAPER_ENV_12</td>
<td>#12 Envelope, 4 3/4- by 11-inches</td>
</tr>
<tr>
<td>DMPAPER_ENV_14</td>
<td>#14 Envelope, 5- by 11 1/2-inches</td>
</tr>
<tr>
<td>DMPAPER_ENV_C5</td>
<td>C5 Envelope, 162- by 229-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_C3</td>
<td>C3 Envelope, 324- by 458-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_C4</td>
<td>C4 Envelope, 229- by 324-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_C6</td>
<td>C6 Envelope, 114- by 162-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_C65</td>
<td>C65 Envelope, 114- by 229-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_B4</td>
<td>B4 Envelope, 250- by 353-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_B5</td>
<td>B5 Envelope, 176- by 250-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_B6</td>
<td>B6 Envelope, 176- by 125-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_DL</td>
<td>DL Envelope, 110- by 220-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_INVITE</td>
<td>Envelope Invite 220 x 220 mm</td>
</tr>
<tr>
<td>DMPAPER_ENV_ITALY</td>
<td>Italy Envelope, 110- by 230-millimeters</td>
</tr>
<tr>
<td>DMPAPER_ENV_MONARCH</td>
<td>Monarch Envelope, 3 7/8- by 7 1/2-inches</td>
</tr>
<tr>
<td>DMPAPER_ENV_PERSONAL</td>
<td>6 3/4 Envelope, 3 5/8- by 6 1/2-inches</td>
</tr>
<tr>
<td>DMPAPER_ESHEET</td>
<td>E Sheet, 34- by 44-inches</td>
</tr>
<tr>
<td>DMPAPER_EXECUTIVE</td>
<td>Executive, 7 1/4- by 10 1/2-inches</td>
</tr>
<tr>
<td>DMPAPER_FANFOLD_US</td>
<td>US Std Fanfold, 14 7/8- by 11-inches</td>
</tr>
<tr>
<td>DMPAPER_FANFOLD_STD_GERMAN</td>
<td>German Std Fanfold, 8 1/2- by 12-inches</td>
</tr>
<tr>
<td>DMPAPER_FANFOLD_LGL_GERMAN</td>
<td>German Legal Fanfold, 8 - by 13-inches</td>
</tr>
<tr>
<td>DMPAPER_FOLIO</td>
<td>Folio, 8 1/2- by 13-inch paper</td>
</tr>
<tr>
<td>DMPAPER_ISO_B4</td>
<td>B4 (ISO) 250- by 353-millimeters paper</td>
</tr>
<tr>
<td>DMPAPER_JAPANESE_POSTCARD</td>
<td>Japanese Postcard, 100- by 148-millimeters</td>
</tr>
<tr>
<td>DMPAPER_JAPANESE_POSTCARD_ROTATED</td>
<td> Japanese Postcard Rotated, 148- by 100-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_CHOU3</td>
<td> Japanese Envelope Chou #3
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_CHOU3_ROTATED</td>
<td> Japanese Envelope Chou #3 Rotated
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_CHOU4</td>
<td> Japanese Envelope Chou #4
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_CHOU4_ROTATED</td>
<td> Japanese Envelope Chou #4 Rotated
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_KAKU2</td>
<td> Japanese Envelope Kaku #2
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_KAKU2_ROTATED</td>
<td> Japanese Envelope Kaku #2 Rotated
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_KAKU3</td>
<td> Japanese Envelope Kaku #3
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_KAKU3_ROTATED</td>
<td> Japanese Envelope Kaku #3 Rotated
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_YOU4</td>
<td> Japanese Envelope You #4
                    </td>
</tr>
<tr>
<td>DMPAPER_JENV_YOU4_ROTATED</td>
<td> Japanese Envelope You #4 Rotated
                    </td>
</tr>
<tr>
<td>DMPAPER_LAST</td>
<td> DMPAPER_PENV_10_ROTATED
                    </td>
</tr>
<tr>
<td>DMPAPER_LEDGER</td>
<td>Ledger, 17- by 11-inches</td>
</tr>
<tr>
<td>DMPAPER_LEGAL_EXTRA</td>
<td>Legal Extra 9 1/2 x 15 inches.</td>
</tr>
<tr>
<td>DMPAPER_LETTER_EXTRA</td>
<td>Letter Extra 9 1/2 x 12 inches.</td>
</tr>
<tr>
<td>DMPAPER_LETTER_EXTRA_TRANSVERSE</td>
<td>Letter Extra Transverse 9 1/2 x 12 inches.</td>
</tr>
<tr>
<td>DMPAPER_LETTER_ROTATED</td>
<td>Letter Rotated 11 by 8 1/2 inches</td>
</tr>
<tr>
<td>DMPAPER_LETTERSMALL</td>
<td>Letter Small, 8 1/2- by 11-inches</td>
</tr>
<tr>
<td>DMPAPER_LETTER_TRANSVERSE</td>
<td>Letter Transverse 8 1/2 x 11-inches</td>
</tr>
<tr>
<td>DMPAPER_NOTE</td>
<td>Note, 8 1/2- by 11-inches</td>
</tr>
<tr>
<td>DMPAPER_P16K</td>
<td> PRC 16K, 146- by 215-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_P16K_ROTATED</td>
<td> PRC 16K Rotated, 215- by 146-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_P32K</td>
<td> PRC 32K, 97- by 151-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_P32K_ROTATED</td>
<td> PRC 32K Rotated, 151- by 97-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_P32KBIG</td>
<td> PRC 32K(Big) 97- by 151-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_P32KBIG_ROTATED</td>
<td> PRC 32K(Big) Rotated, 151- by 97-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_1</td>
<td> PRC Envelope #1, 102- by 165-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_1_ROTATED</td>
<td> PRC Envelope #1 Rotated, 165- by 102-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_2</td>
<td> PRC Envelope #2, 102- by 176-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_2_ROTATED</td>
<td> PRC Envelope #2 Rotated, 176- by 102-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_3</td>
<td> PRC Envelope #3, 125- by 176-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_3_ROTATED</td>
<td> PRC Envelope #3 Rotated, 176- by 125-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_4</td>
<td> PRC Envelope #4, 110- by 208-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_4_ROTATED</td>
<td> PRC Envelope #4 Rotated, 208- by 110-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_5</td>
<td> PRC Envelope #5, 110- by 220-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_5_ROTATED</td>
<td> PRC Envelope #5 Rotated, 220- by 110-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_6</td>
<td> PRC Envelope #6, 120- by 230-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_6_ROTATED</td>
<td> PRC Envelope #6 Rotated, 230- by 120-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_7</td>
<td> PRC Envelope #7, 160- by 230-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_7_ROTATED</td>
<td> PRC Envelope #7 Rotated, 230- by 160-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_8</td>
<td> PRC Envelope #8, 120- by 309-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_8_ROTATED</td>
<td> PRC Envelope #8 Rotated, 309- by 120-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_9</td>
<td> PRC Envelope #9, 229- by 324-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_9_ROTATED</td>
<td> PRC Envelope #9 Rotated, 324- by 229-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_10</td>
<td> PRC Envelope #10, 324- by 458-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_PENV_10_ROTATED</td>
<td> PRC Envelope #10 Rotated, 458- by 324-millimeters
                    </td>
</tr>
<tr>
<td>DMPAPER_QUARTO</td>
<td>Quarto, 215- by 275-millimeter paper</td>
</tr>
<tr>
<td>DMPAPER_STATEMENT</td>
<td>Statement, 5 1/2- by 8 1/2-inches</td>
</tr>
<tr>
<td>DMPAPER_TABLOID</td>
<td>Tabloid, 11- by 17-inches</td>
</tr>
<tr>
<td>DMPAPER_TABLOID_EXTRA</td>
<td>Tabloid, 11.69 x 18-inches</td>
</tr>
</table>

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmPaperLength

For printer devices only, overrides the length of the paper specified by the <b>dmPaperSize</b> member, either for custom paper sizes or for devices such as dot-matrix printers that can print on a page of arbitrary length. These values, along with all other values in this structure that specify a physical length, are in tenths of a millimeter.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmPaperWidth

For printer devices only, overrides the width of the paper specified by the <b>dmPaperSize</b> member.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmScale

Specifies the factor by which the printed output is to be scaled. The apparent page size is scaled from the physical page size by a factor of <b>dmScale</b> /100. For example, a letter-sized page with a <b>dmScale</b> value of 50 would contain as much data as a page of 17- by 22-inches because the output text and graphics would be half their original height and width.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmCopies

Selects the number of copies printed if the device supports multiple-page copies.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmDefaultSource

Specifies the paper source. To retrieve a list of the available paper sources for a printer, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa">DeviceCapabilities</a> function with the DC_BINS flag.

This member can be one of the following values, or it can be a device-specific value greater than or equal to DMBIN_USER.

<a id="DMBIN_AUTO"></a>
<a id="dmbin_auto"></a>

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.dmPrintQuality

Specifies the printer resolution. There are four predefined device-independent values:

<a id="DMRES_HIGH"></a>
<a id="dmres_high"></a>
If a positive value is specified, it specifies the number of dots per inch (DPI) and is therefore device dependent.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME2

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME2.dmPosition

For display devices only, a <a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a> structure that indicates the positional coordinates of the display device in reference to the desktop area. The primary display device is always located at coordinates (0,0).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME2.dmDisplayOrientation

For display devices only, the orientation at which images should be presented. If DM_DISPLAYORIENTATION is not set, this member must be zero. If DM_DISPLAYORIENTATION is set, this member must be one of the following values

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMDO_DEFAULT</td>
<td>The display orientation is the natural orientation of the display device; it should be used as the default.</td>
</tr>
<tr>
<td>DMDO_90</td>
<td>The display orientation is rotated 90 degrees (measured counter-clockwise) from DMDO_DEFAULT.</td>
</tr>
<tr>
<td>DMDO_180</td>
<td>The display orientation is rotated 180 degrees (measured counter-clockwise) from DMDO_DEFAULT.</td>
</tr>
<tr>
<td>DMDO_270</td>
<td>The display orientation is rotated 270 degrees (measured counter-clockwise) from DMDO_DEFAULT.</td>
</tr>
</table>
 

To determine whether the display orientation is portrait or landscape orientation, check the ratio of <b>dmPelsWidth</b> to <b>dmPelsHeight</b>.
                

<b>Windows 2000:  </b>Not supported.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME2.dmDisplayFixedOutput

For fixed-resolution display devices only, how the display presents a low-resolution mode on a higher-resolution display. For example, if a display device's resolution is fixed at 1024 x 768 pixels but its mode is set to 640 x 480 pixels, the device can either display a 640 x 480 image somewhere in the interior of the 1024 x 768 screen space or stretch the 640 x 480 image to fill the larger screen space. If DM_DISPLAYFIXEDOUTPUT is not set, this member must be zero. If DM_DISPLAYFIXEDOUTPUT is set, this member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMDFO_DEFAULT</td>
<td>The display's default setting.</td>
</tr>
<tr>
<td>DMDFO_CENTER</td>
<td>The low-resolution image is centered in the larger screen space.</td>
</tr>
<tr>
<td>DMDFO_STRETCH</td>
<td>The low-resolution image is stretched to fill the larger screen space.</td>
</tr>
</table>
 

<b>Windows 2000:  </b>Not supported.

### -field dmColor

Switches between color and monochrome on color printers. The following are the possible values:

<ul>
<li>DMCOLOR_COLOR</li>
<li>DMCOLOR_MONOCHROME</li>
</ul>

### -field dmDuplex

Selects duplex or double-sided printing for printers capable of duplex printing. Following are the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMDUP_SIMPLEX</td>
<td>Normal (nonduplex) printing.</td>
</tr>
<tr>
<td>DMDUP_HORIZONTAL</td>
<td>Short-edge binding, that is, the long edge of the page is horizontal.</td>
</tr>
<tr>
<td>DMDUP_VERTICAL</td>
<td>Long-edge binding, that is, the long edge of the page is vertical.</td>
</tr>
</table>

### -field dmYResolution

Specifies the y-resolution, in dots per inch, of the printer. If the printer initializes this member, the <b>dmPrintQuality</b> member specifies the x-resolution, in dots per inch, of the printer.

### -field dmTTOption

Specifies how TrueType fonts should be printed. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMTT_BITMAP</td>
<td>Prints TrueType fonts as graphics. This is the default action for dot-matrix printers.</td>
</tr>
<tr>
<td>DMTT_DOWNLOAD</td>
<td>Downloads TrueType fonts as soft fonts. This is the default action for Hewlett-Packard printers that use Printer Control Language (PCL).</td>
</tr>
<tr>
<td>DMTT_DOWNLOAD_OUTLINE</td>
<td> Downloads TrueType fonts as outline soft fonts.
                </td>
</tr>
<tr>
<td>DMTT_SUBDEV</td>
<td>Substitutes device fonts for TrueType fonts. This is the default action for PostScript printers.</td>
</tr>
</table>

### -field dmCollate

Specifies whether collation should be used when printing multiple copies. (This member is ignored unless the printer driver indicates support for collation by setting the <b>dmFields</b> member to DM_COLLATE.) This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMCOLLATE_TRUE</td>
<td>Collate when printing multiple copies.</td>
</tr>
<tr>
<td>DMCOLLATE_FALSE</td>
<td>Do not collate when printing multiple copies.</td>
</tr>
</table>

### -field dmFormName

A zero-terminated character array that specifies the name of the form to use; for example, "Letter" or "Legal". A complete set of names can be retrieved by using the <a href="/windows/desktop/printdocs/enumforms">EnumForms</a> function.

### -field dmLogPixels

The number of pixels per logical inch. Printer drivers do not use this member.

### -field dmBitsPerPel

Specifies the color resolution, in bits per pixel, of the display device (for example: 4 bits for 16 colors, 8 bits for 256 colors, or 16 bits for 65,536 colors). Display drivers use this member, for example, in the <a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a> function. Printer drivers do not use this member.

### -field dmPelsWidth

Specifies the width, in pixels, of the visible device surface. Display drivers use this member, for example, in the <a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a> function. Printer drivers do not use this member.

### -field dmPelsHeight

Specifies the height, in pixels, of the visible device surface. Display drivers use this member, for example, in the <a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a> function. Printer drivers do not use this member.

### -field DUMMYUNIONNAME2

### -field DUMMYUNIONNAME2.dmDisplayFlags

Specifies the device's display mode. This member can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DM_GRAYSCALE</td>
<td>Specifies that the display is a noncolor device. If this flag is not set, color is assumed. This flag is no longer valid.</td>
</tr>
<tr>
<td>DM_INTERLACED</td>
<td>Specifies that the display mode is interlaced. If the flag is not set, noninterlaced is assumed.</td>
</tr>
</table>
 

Display drivers use this member, for example, in the <a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a> function. Printer drivers do not use this member.

### -field DUMMYUNIONNAME2.dmNup

Specifies where the NUP is done. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMNUP_SYSTEM</td>
<td>The print spooler does the NUP.</td>
</tr>
<tr>
<td>DMNUP_ONEUP</td>
<td>The application does the NUP.</td>
</tr>
</table>

### -field dmDisplayFrequency

Specifies the frequency, in hertz (cycles per second), of the display device in a particular mode. This value is also known as the display device's vertical refresh rate. Display drivers use this member. It is used, for example, in the <a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a> function. Printer drivers do not use this member.

When you call the <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa">EnumDisplaySettings</a> function, the <b>dmDisplayFrequency</b> member may return with the value 0 or 1. These values represent the display hardware's default refresh rate. This default rate is typically set by switches on a display card or computer motherboard, or by a configuration program that does not use display functions such as <a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a>.

### -field dmICMMethod

Specifies how ICM is handled. For a non-ICM application, this member determines if ICM is enabled or disabled. For ICM applications, the system examines this member to determine how to handle ICM support. This member can be one of the following predefined values, or a driver-defined value greater than or equal to the value of DMICMMETHOD_USER.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMICMMETHOD_NONE</td>
<td>Specifies that ICM is disabled.</td>
</tr>
<tr>
<td>DMICMMETHOD_SYSTEM</td>
<td>Specifies that ICM is handled by Windows.</td>
</tr>
<tr>
<td>DMICMMETHOD_DRIVER</td>
<td>Specifies that ICM is handled by the device driver.</td>
</tr>
<tr>
<td>DMICMMETHOD_DEVICE</td>
<td>Specifies that ICM is handled by the destination device.</td>
</tr>
</table>
 

The printer driver must provide a user interface for setting this member. Most printer drivers support only the DMICMMETHOD_SYSTEM or DMICMMETHOD_NONE value. Drivers for PostScript printers support all values.

### -field dmICMIntent

Specifies which color matching method, or intent, should be used by default. This member is primarily for non-ICM applications. ICM applications can establish intents by using the ICM functions. This member can be one of the following predefined values, or a driver defined value greater than or equal to the value of DMICM_USER.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMICM_ABS_COLORIMETRIC</td>
<td>Color matching should optimize to match the exact color requested without white point mapping. This value is most appropriate for use with proofing.</td>
</tr>
<tr>
<td>DMICM_COLORIMETRIC</td>
<td>Color matching should optimize to match the exact color requested. This value is most appropriate for use with business logos or other images when an exact color match is desired.</td>
</tr>
<tr>
<td>DMICM_CONTRAST</td>
<td>Color matching should optimize for color contrast. This value is the most appropriate choice for scanned or photographic images when dithering is desired.</td>
</tr>
<tr>
<td>DMICM_SATURATE</td>
<td>Color matching should optimize for color saturation. This value is the most appropriate choice for business graphs when dithering is not desired.</td>
</tr>
</table>

### -field dmMediaType

Specifies the type of media being printed on. The member can be one of the following predefined values, or a driver-defined value greater than or equal to the value of DMMEDIA_USER.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMMEDIA_STANDARD</td>
<td>Plain paper.</td>
</tr>
<tr>
<td>DMMEDIA_GLOSSY</td>
<td>Glossy paper.</td>
</tr>
<tr>
<td>DMMEDIA_TRANSPARENCY</td>
<td>Transparent film.</td>
</tr>
</table>
 

 To retrieve a list of the available media types for a printer, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa">DeviceCapabilities</a> function with the DC_MEDIATYPES flag.

### -field dmDitherType

Specifies how dithering is to be done. The member can be one of the following predefined values, or a driver-defined value greater than or equal to the value of DMDITHER_USER.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DMDITHER_NONE</td>
<td>No dithering.</td>
</tr>
<tr>
<td>DMDITHER_COARSE</td>
<td>Dithering with a coarse brush.</td>
</tr>
<tr>
<td>DMDITHER_FINE</td>
<td>Dithering with a fine brush.</td>
</tr>
<tr>
<td>DMDITHER_LINEART</td>
<td>Line art dithering, a special dithering method that produces well defined borders between black, white, and gray scaling. It is not suitable for images that include continuous graduations in intensity and hue, such as scanned photographs.</td>
</tr>
<tr>
<td>DMDITHER_GRAYSCALE</td>
<td>Device does gray scaling.</td>
</tr>
</table>

### -field dmReserved1

Not used; must be zero.

### -field dmReserved2

Not used; must be zero.

### -field dmPanningWidth

This member must be zero.

### -field dmPanningHeight

This member must be zero.


##### - dmDefaultSource.DMBIN_AUTO

<a id="DMBIN_CASSETTE"></a>
<a id="dmbin_cassette"></a>

##### - dmDefaultSource.DMBIN_CASSETTE

<a id="DMBIN_ENVELOPE"></a>
<a id="dmbin_envelope"></a>

##### - dmDefaultSource.DMBIN_ENVELOPE

<a id="DMBIN_ENVMANUAL"></a>
<a id="dmbin_envmanual"></a>

##### - dmDefaultSource.DMBIN_ENVMANUAL

<a id="DMBIN_FIRST"></a>
<a id="dmbin_first"></a>

##### - dmDefaultSource.DMBIN_FIRST

<a id="DMBIN_FORMSOURCE"></a>
<a id="dmbin_formsource"></a>

##### - dmDefaultSource.DMBIN_FORMSOURCE

<a id="DMBIN_LARGECAPACITY"></a>
<a id="dmbin_largecapacity"></a>

##### - dmDefaultSource.DMBIN_LARGECAPACITY

<a id="DMBIN_LARGEFMT"></a>
<a id="dmbin_largefmt"></a>

##### - dmDefaultSource.DMBIN_LARGEFMT

<a id="DMBIN_LAST"></a>
<a id="dmbin_last"></a>

##### - dmDefaultSource.DMBIN_LAST

<a id="DMBIN_LOWER"></a>
<a id="dmbin_lower"></a>

##### - dmDefaultSource.DMBIN_LOWER

<a id="DMBIN_MANUAL"></a>
<a id="dmbin_manual"></a>

##### - dmDefaultSource.DMBIN_MANUAL

<a id="DMBIN_MIDDLE"></a>
<a id="dmbin_middle"></a>

##### - dmDefaultSource.DMBIN_MIDDLE

<a id="DMBIN_ONLYONE"></a>
<a id="dmbin_onlyone"></a>

##### - dmDefaultSource.DMBIN_ONLYONE

<a id="DMBIN_TRACTOR"></a>
<a id="dmbin_tractor"></a>

##### - dmDefaultSource.DMBIN_SMALLFMT

<a id="DMBIN_UPPER"></a>
<a id="dmbin_upper"></a>

##### - dmDefaultSource.DMBIN_TRACTOR

<a id="DMBIN_SMALLFMT"></a>
<a id="dmbin_smallfmt"></a>

##### - dmDefaultSource.DMBIN_UPPER


##### - dmPrintQuality.DMRES_DRAFT


##### - dmPrintQuality.DMRES_HIGH

<a id="DMRES_MEDIUM"></a>
<a id="dmres_medium"></a>

##### - dmPrintQuality.DMRES_LOW

<a id="DMRES_DRAFT"></a>
<a id="dmres_draft"></a>

##### - dmPrintQuality.DMRES_MEDIUM

<a id="DMRES_LOW"></a>
<a id="dmres_low"></a>

## -remarks

A device driver's private data follows the public portion of the <b>DEVMODE</b> structure. The size of the public data can vary for different versions of the structure. The <b>dmSize</b> member specifies the number of bytes of public data, and the <b>dmDriverExtra</b> member specifies the number of bytes of private data.
      





> [!NOTE]
> The wingdi.h header defines DEVMODE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/printdocs/advanceddocumentproperties">AdvancedDocumentProperties</a>



<a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createica">CreateIC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa">DeviceCapabilities</a>



<a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa">EnumDisplaySettings</a>



<a href="/windows/desktop/printdocs/openprinter">OpenPrinter</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-structures">Print Spooler API Structures</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>
