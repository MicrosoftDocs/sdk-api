---
UID: NS:winuser.tagICONMETRICSA
title: ICONMETRICSA (winuser.h)
author: windows-sdk-content
description: Contains the scalable metrics associated with icons. This structure is used with the SystemParametersInfo function when the SPI_GETICONMETRICS or SPI_SETICONMETRICS action is specified.
old-location: menurc\iconmetrics.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconstructures\iconmetrics.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPICONMETRICSA, *PICONMETRICSA, ICONMETRICS, ICONMETRICS structure [Menus and Other Resources], ICONMETRICSA, ICONMETRICSW, LPICONMETRICS, LPICONMETRICS structure pointer [Menus and Other Resources], PICONMETRICS, PICONMETRICS structure pointer [Menus and Other Resources], _win32_ICONMETRICS_str, _win32_iconmetrics_str_cpp, menurc.iconmetrics, winui._win32_iconmetrics_str, winuser/ICONMETRICS, winuser/ICONMETRICSA, winuser/ICONMETRICSW, winuser/LPICONMETRICS, winuser/PICONMETRICS"
ms.topic: struct
f1_keywords: 
 - "winuser/ICONMETRICS"
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ICONMETRICSW (Unicode) and ICONMETRICSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - ICONMETRICS
 - ICONMETRICSA
 - ICONMETRICSW
targetos: Windows
req.typenames: ICONMETRICSA, *PICONMETRICSA, *LPICONMETRICSA
req.redist: 
ms.custom: 19H1
---

# ICONMETRICSA structure


## -description


Contains the scalable metrics associated with icons. This structure is used with the  <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function when the <b>SPI_GETICONMETRICS</b>  or <b>SPI_SETICONMETRICS</b> action is specified.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of the structure, in bytes. 


### -field iHorzSpacing

Type: <b>int</b>

The horizontal space, in pixels, for each arranged icon. 


### -field iVertSpacing

Type: <b>int</b>

The vertical space, in pixels, for each arranged icon. 


### -field iTitleWrap

Type: <b>int</b>

If this member is nonzero, icon titles wrap to a new line. If this member is zero, titles do not wrap. 


### -field lfFont

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a></b>

The font to use for icon titles. 


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/icons">Icons</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>
 

 

