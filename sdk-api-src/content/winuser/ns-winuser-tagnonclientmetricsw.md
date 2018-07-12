---
UID: NS:winuser.tagNONCLIENTMETRICSW
title: tagNONCLIENTMETRICSW
author: windows-sdk-content
description: Contains the scalable metrics associated with the nonclient area of a nonminimized window.
old-location: winmsg\nonclientmetrics_str.htm
old-project: winmsg
ms.assetid: 663d3aff-1764-4bc4-96f5-809ddb4e9348
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*LPNONCLIENTMETRICSW, *PNONCLIENTMETRICSW, LPNONCLIENTMETRICS, LPNONCLIENTMETRICS structure pointer [Windows and Messages], NONCLIENTMETRICS, NONCLIENTMETRICS structure [Windows and Messages], NONCLIENTMETRICSA, NONCLIENTMETRICSW, PNONCLIENTMETRICS, PNONCLIENTMETRICS structure pointer [Windows and Messages], _win32_nonclientmetrics_str, base.nonclientmetrics_str, nonclientmetrics_str_cpp, tagNONCLIENTMETRICS, tagNONCLIENTMETRICSW, winmsg.nonclientmetrics_str, winui.nonclientmetrics_str, winuser/LPNONCLIENTMETRICS, winuser/NONCLIENTMETRICS, winuser/NONCLIENTMETRICSA, winuser/NONCLIENTMETRICSW, winuser/PNONCLIENTMETRICS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: NONCLIENTMETRICSW, *PNONCLIENTMETRICSW, *LPNONCLIENTMETRICSW
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagNONCLIENTMETRICSW structure


## -description


Contains the scalable metrics associated with the nonclient area of a nonminimized window. This structure is used by the <b>SPI_GETNONCLIENTMETRICS</b> and <b>SPI_SETNONCLIENTMETRICS</b> actions of 
the <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function.


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

A <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure that contains information about the caption font.


### -field iSmCaptionWidth

The width of small caption buttons, in pixels.


### -field iSmCaptionHeight

The height of small captions, in pixels.


### -field lfSmCaptionFont

A <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure that contains information about the small caption font.


### -field iMenuWidth

The width of menu-bar buttons, in pixels.


### -field iMenuHeight

The height of a menu bar, in pixels.


### -field lfMenuFont

A <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure that contains information about the font used in menu bars.


### -field lfStatusFont

A <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure that contains information about the font used in status bars and tooltips.


### -field lfMessageFont

A <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure that contains information about the font used in message boxes.


### -field iPaddedBorderWidth

The thickness of the padded border, in pixels. The default value is 4 pixels. The <b>iPaddedBorderWidth</b> and <b>iBorderWidth</b> members are combined for both resizable and nonresizable windows in  the Windows Aero desktop experience. To compile an application that uses this member, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see Remarks. 

<b>Windows Server 2003 and Windows XP/2000:  </b>This member is not supported.


## -remarks



If the <b>iPaddedBorderWidth</b> member of the <a href="https://msdn.microsoft.com/663d3aff-1764-4bc4-96f5-809ddb4e9348">NONCLIENTMETRICS</a> structure is present, this structure is 4 bytes larger than for an application that is compiled with <b>_WIN32_WINNT</b> less than or equal to 0x0502. For more information about conditional compilation, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.

<b>Windows Server 2003 and Windows XP/2000:  </b>If an application  that is compiled for Windows Server 2008 or Windows Vista must also run on Windows Server 2003 or Windows XP/2000, use the <a href="https://msdn.microsoft.com/8e3ab4d6-bacd-4bc5-b8f6-dd49289354de">GetVersionEx</a> function to check the operating system version at run time and, if the application is running on Windows Server 2003 or Windows XP/2000, subtract the size of the <b>iPaddedBorderWidth</b> member from the <b>cbSize</b> member of the <a href="https://msdn.microsoft.com/663d3aff-1764-4bc4-96f5-809ddb4e9348">NONCLIENTMETRICS</a> structure before calling the <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 

