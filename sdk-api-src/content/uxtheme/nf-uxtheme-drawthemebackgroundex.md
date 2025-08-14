---
UID: NF:uxtheme.DrawThemeBackgroundEx
title: DrawThemeBackgroundEx function (uxtheme.h)
description: Draws the background image defined by the visual style for the specified control part.
helpviewer_keywords: ["DrawThemeBackgroundEx","DrawThemeBackgroundEx function [Windows Controls]","controls.DrawThemeBackgroundEx","controls.inet_DrawThemeBackgroundEx","inet_DrawThemeBackgroundEx","inet_DrawThemeBackgroundEx_cpp","uxtheme/DrawThemeBackgroundEx"]
old-location: controls\DrawThemeBackgroundEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemebackgroundex.htm
ms.date: 12/05/2018
ms.keywords: DrawThemeBackgroundEx, DrawThemeBackgroundEx function [Windows Controls], controls.DrawThemeBackgroundEx, controls.inet_DrawThemeBackgroundEx, inet_DrawThemeBackgroundEx, inet_DrawThemeBackgroundEx_cpp, uxtheme/DrawThemeBackgroundEx
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawThemeBackgroundEx
 - uxtheme/DrawThemeBackgroundEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - ext-ms-win-uxtheme-themes-l1-1-2.dll
 - UxTheme.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - DrawThemeBackgroundEx
---

# DrawThemeBackgroundEx function


## -description

<p class="CCE_Message">[<b>DrawThemeBackgroundEx</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Draws the background image defined by the visual style for the specified control part.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC used for drawing the theme-defined background image.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part to draw. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part to draw. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param pRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle, in logical coordinates, in which the background image is drawn.

### -param pOptions [in]

Type: <b>const <a href="/windows/desktop/api/uxtheme/ns-uxtheme-dtbgopts">DTBGOPTS</a>*</b>

Pointer to a <a href="/windows/desktop/api/uxtheme/ns-uxtheme-dtbgopts">DTBGOPTS</a> structure that contains clipping information. This parameter may be set to <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Drawing operations are scaled to fit and to not exceed the rectangle specified in <i>pRect</i>.