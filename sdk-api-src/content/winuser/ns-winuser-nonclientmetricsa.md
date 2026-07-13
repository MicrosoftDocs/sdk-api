---
UID: NS:winuser.tagNONCLIENTMETRICSA
title: NONCLIENTMETRICSA (winuser.h)
description: Contains the scalable metrics associated with the nonclient area of a nonminimized window. (ANSI)
helpviewer_keywords: ["*LPNONCLIENTMETRICSA","*PNONCLIENTMETRICSA","LPNONCLIENTMETRICS","LPNONCLIENTMETRICS structure pointer [Windows and Messages]","NONCLIENTMETRICS","NONCLIENTMETRICS structure [Windows and Messages]","NONCLIENTMETRICSA","NONCLIENTMETRICSW","PNONCLIENTMETRICS","PNONCLIENTMETRICS structure pointer [Windows and Messages]","_win32_nonclientmetrics_str","base.nonclientmetrics_str","nonclientmetrics_str_cpp","tagNONCLIENTMETRICS","winmsg.nonclientmetrics_str","winui.nonclientmetrics_str","winuser/LPNONCLIENTMETRICS","winuser/NONCLIENTMETRICS","winuser/NONCLIENTMETRICSA","winuser/NONCLIENTMETRICSW","winuser/PNONCLIENTMETRICS"]
old-location: winmsg\nonclientmetrics_str.htm
tech.root: winmsg
ms.assetid: 663d3aff-1764-4bc4-96f5-809ddb4e9348
ms.date: 12/05/2018
ms.keywords: '*LPNONCLIENTMETRICSA, *PNONCLIENTMETRICSA, LPNONCLIENTMETRICS, LPNONCLIENTMETRICS structure pointer [Windows and Messages], NONCLIENTMETRICS, NONCLIENTMETRICS structure [Windows and Messages], NONCLIENTMETRICSA, NONCLIENTMETRICSW, PNONCLIENTMETRICS, PNONCLIENTMETRICS structure pointer [Windows and Messages], _win32_nonclientmetrics_str, base.nonclientmetrics_str, nonclientmetrics_str_cpp, tagNONCLIENTMETRICS, winmsg.nonclientmetrics_str, winui.nonclientmetrics_str, winuser/LPNONCLIENTMETRICS, winuser/NONCLIENTMETRICS, winuser/NONCLIENTMETRICSA, winuser/NONCLIENTMETRICSW, winuser/PNONCLIENTMETRICS'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NONCLIENTMETRICSW (Unicode) and NONCLIENTMETRICSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NONCLIENTMETRICSA, *PNONCLIENTMETRICSA, *LPNONCLIENTMETRICSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNONCLIENTMETRICSA
 - winuser/tagNONCLIENTMETRICSA
 - PNONCLIENTMETRICSA
 - winuser/PNONCLIENTMETRICSA
 - NONCLIENTMETRICSA
 - winuser/NONCLIENTMETRICSA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - NONCLIENTMETRICS
 - NONCLIENTMETRICSA
 - NONCLIENTMETRICSW
---

# NONCLIENTMETRICSA structure


## -description

Contains the scalable metrics associated with the nonclient area of a nonminimized window. This structure is used by the <b>SPI_GETNONCLIENTMETRICS</b> and <b>SPI_SETNONCLIENTMETRICS</b> actions of 
the <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function.

## -struct-fields

### -field cbSize

The size of the structure, in bytes. The caller must set this to <code>sizeof(NONCLIENTMETRICS)</code>. For   information about application compatibility, see Remarks.

### -field iBorderWidth

The thickness of the sizing border, in pixels. The default is 1 pixel.

### -field iScrollWidth

The width of a standard vertical scroll bar, in pixels.

### -field iScrollHeight

The height of a standard horizontal scroll bar, in pixels.

### -field iCaptionWidth

The width of caption buttons, in pixels.

### -field iCaptionHeight

The height of caption buttons, in pixels.

### -field lfCaptionFont

A <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that contains information about the caption font.

### -field iSmCaptionWidth

The width of small caption buttons, in pixels.

### -field iSmCaptionHeight

The height of small captions, in pixels.

### -field lfSmCaptionFont

A <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that contains information about the small caption font.

### -field iMenuWidth

The width of menu-bar buttons, in pixels.

### -field iMenuHeight

The height of a menu bar, in pixels.

### -field lfMenuFont

A <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that contains information about the font used in menu bars.

### -field lfStatusFont

A <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that contains information about the font used in status bars and tooltips.

### -field lfMessageFont

A <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that contains information about the font used in message boxes.

### -field iPaddedBorderWidth

The thickness of the padded border, in pixels. The default value is 4 pixels. The <b>iPaddedBorderWidth</b> and <b>iBorderWidth</b> members are combined for both resizable and nonresizable windows in  the Windows Aero desktop experience. To compile an application that uses this member, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see Remarks. 

<b>Windows Server 2003 and Windows XP/2000:  </b>This member is not supported.

## -remarks

If the <b>iPaddedBorderWidth</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-nonclientmetricsa">NONCLIENTMETRICS</a> structure is present, this structure is 4 bytes larger than for an application that is compiled with <b>_WIN32_WINNT</b> less than or equal to 0x0502. For more information about conditional compilation, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

<b>Windows Server 2003 and Windows XP/2000:  </b>If an application  that is compiled for Windows Server 2008 or Windows Vista must also run on Windows Server 2003 or Windows XP/2000, use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa">GetVersionEx</a> function to check the operating system version at run time and, if the application is running on Windows Server 2003 or Windows XP/2000, subtract the size of the <b>iPaddedBorderWidth</b> member from the <b>cbSize</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-nonclientmetricsa">NONCLIENTMETRICS</a> structure before calling the <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function. 





> [!NOTE]
> The winuser.h header defines NONCLIENTMETRICS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>
