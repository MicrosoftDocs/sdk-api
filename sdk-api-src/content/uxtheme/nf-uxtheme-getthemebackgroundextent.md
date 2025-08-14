---
UID: NF:uxtheme.GetThemeBackgroundExtent
title: GetThemeBackgroundExtent function (uxtheme.h)
description: Calculates the size and location of the background, defined by the visual style, given the content area.
helpviewer_keywords: ["GetThemeBackgroundExtent","GetThemeBackgroundExtent function [Windows Controls]","controls.GetThemeBackgroundExtent","controls.inet_GetThemeBackgroundExtent","inet_GetThemeBackgroundExtent","inet_GetThemeBackgroundExtent_cpp","uxtheme/GetThemeBackgroundExtent"]
old-location: controls\GetThemeBackgroundExtent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemebackgroundextent.htm
ms.date: 12/05/2018
ms.keywords: GetThemeBackgroundExtent, GetThemeBackgroundExtent function [Windows Controls], controls.GetThemeBackgroundExtent, controls.inet_GetThemeBackgroundExtent, inet_GetThemeBackgroundExtent, inet_GetThemeBackgroundExtent_cpp, uxtheme/GetThemeBackgroundExtent
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
 - GetThemeBackgroundExtent
 - uxtheme/GetThemeBackgroundExtent
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
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - GetThemeBackgroundExtent
---

# GetThemeBackgroundExtent function


## -description

Calculates the size and location of the background, defined by the visual style, given the content area.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC to use when drawing. This parameter may be set to <b>NULL</b>.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the content. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part that contains the content. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param pContentRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the content background rectangle, in logical coordinates. This rectangle is returned from <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemebackgroundcontentrect">GetThemeBackgroundContentRect</a>.

### -param pExtentRect [out]

Type: <b>LPRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the background rectangle, in logical coordinates. This rectangle is based on the <i>pContentRect</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A theme can define a content area within each background image. This is the area where content such as text and icons can be placed without overwriting background borders.

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemebackgroundcontentrect">GetThemeBackgroundContentRect</a>



<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>



<b>Reference</b>