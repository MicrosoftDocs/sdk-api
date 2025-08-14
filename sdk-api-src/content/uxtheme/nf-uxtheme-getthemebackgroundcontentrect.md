---
UID: NF:uxtheme.GetThemeBackgroundContentRect
title: GetThemeBackgroundContentRect function (uxtheme.h)
description: Retrieves the size of the content area for the background defined by the visual style.
helpviewer_keywords: ["GetThemeBackgroundContentRect","GetThemeBackgroundContentRect function [Windows Controls]","controls.GetThemeBackgroundContentRect","controls.inet_GetThemeBackgroundContentRect","inet_GetThemeBackgroundContentRect","inet_GetThemeBackgroundContentRect_cpp","uxtheme/GetThemeBackgroundContentRect"]
old-location: controls\GetThemeBackgroundContentRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemebackgroundcontentrect.htm
ms.date: 12/05/2018
ms.keywords: GetThemeBackgroundContentRect, GetThemeBackgroundContentRect function [Windows Controls], controls.GetThemeBackgroundContentRect, controls.inet_GetThemeBackgroundContentRect, inet_GetThemeBackgroundContentRect, inet_GetThemeBackgroundContentRect_cpp, uxtheme/GetThemeBackgroundContentRect
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
 - GetThemeBackgroundContentRect
 - uxtheme/GetThemeBackgroundContentRect
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
 - GetThemeBackgroundContentRect
---

# GetThemeBackgroundContentRect function


## -description

Retrieves the size of the content area for the background defined by the visual style.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC to use when drawing. This parameter may be set to <b>NULL</b>.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the content area. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part that contains the content area. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param pBoundingRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the total background rectangle, in logical coordinates. This is the area inside the borders or margins.

### -param pContentRect [out]

Type: <b>LPRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the content area background rectangle, in logical coordinates.  This rectangle is calculated to fit the content area.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A visual style can define a content area within each background image. This is the area where content such as text and icons can be placed without overwriting background borders.


#### Examples

When applying a theme to an entire client area of a window, you can call <a href="/windows/desktop/api/winuser/nf-winuser-getclientrect">GetClientRect</a> to retrieve this area in a <b>RECT</b>, which can be passed via pointer as the <i>pContentRect</i> parameter to <b>GetThemeBackgroundContentRect</b> as in the following example.
		


```cpp
DWORD resultFlags = GetThemeAppProperties();
bool ctrlsAreThemed = ((resultFlags & STAP_ALLOW_CONTROLS) != 0);

```

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemebackgroundextent">GetThemeBackgroundExtent</a>



<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>



<b>Reference</b>