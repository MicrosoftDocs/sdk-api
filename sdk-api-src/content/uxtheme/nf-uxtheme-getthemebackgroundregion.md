---
UID: NF:uxtheme.GetThemeBackgroundRegion
title: GetThemeBackgroundRegion function (uxtheme.h)
description: Computes the region for a regular or partially transparent background that is bounded by a specified rectangle.
helpviewer_keywords: ["GetThemeBackgroundRegion","GetThemeBackgroundRegion function [Windows Controls]","controls.GetThemeBackgroundRegion","controls.inet_GetThemeBackgroundRegion","inet_GetThemeBackgroundRegion","inet_GetThemeBackgroundRegion_cpp","uxtheme/GetThemeBackgroundRegion"]
old-location: controls\GetThemeBackgroundRegion.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemebackgroundregion.htm
ms.date: 12/05/2018
ms.keywords: GetThemeBackgroundRegion, GetThemeBackgroundRegion function [Windows Controls], controls.GetThemeBackgroundRegion, controls.inet_GetThemeBackgroundRegion, inet_GetThemeBackgroundRegion, inet_GetThemeBackgroundRegion_cpp, uxtheme/GetThemeBackgroundRegion
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
 - GetThemeBackgroundRegion
 - uxtheme/GetThemeBackgroundRegion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetThemeBackgroundRegion
---

# GetThemeBackgroundRegion function


## -description

Computes the region for a regular or partially transparent background that is bounded by a specified rectangle.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC to draw into. The DC uses dots per inch (DPI) scaling. This parameter may be set to <b>NULL</b>.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the region. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param pRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains, in logical coordinates, the specified rectangle used to compute the region.

### -param pRegion [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRGN</a>*</b>

Pointer to the handle to the computed <a href="/windows/desktop/gdi/regions">region</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The region handle that is returned by this function should be released when it is no longer needed, using <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>.

## -see-also

<b>Other Resources</b>



<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>



<b>Reference</b>



<a href="/windows/desktop/gdi/regions">Regions</a>