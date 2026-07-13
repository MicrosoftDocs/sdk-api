---
UID: NF:uxtheme.HitTestThemeBackground
title: HitTestThemeBackground function (uxtheme.h)
description: Retrieves a hit test code for a point in the background specified by a visual style.
helpviewer_keywords: ["HitTestThemeBackground","HitTestThemeBackground function [Windows Controls]","controls.HitTestThemeBackground","controls.inet_HitTestThemeBackground","inet_HitTestThemeBackground","inet_HitTestThemeBackground_cpp","uxtheme/HitTestThemeBackground"]
old-location: controls\HitTestThemeBackground.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\hittestthemebackground.htm
ms.date: 12/05/2018
ms.keywords: HitTestThemeBackground, HitTestThemeBackground function [Windows Controls], controls.HitTestThemeBackground, controls.inet_HitTestThemeBackground, inet_HitTestThemeBackground, inet_HitTestThemeBackground_cpp, uxtheme/HitTestThemeBackground
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
 - HitTestThemeBackground
 - uxtheme/HitTestThemeBackground
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
 - HitTestThemeBackground
---

# HitTestThemeBackground function


## -description

Retrieves a hit test code for a point in the background specified by a visual style.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC to use when drawing. This parameter may be set to <b>NULL</b>.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param dwOptions [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<b>DWORD</b> that specifies the hit test options. See <a href="/windows/desktop/Controls/theme-hit-test-options">Hit Test Options</a> for a list of options.

### -param pRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains, in logical coordinates, the rectangle that bounds the background.

### -param hrgn [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRGN</a></b>

Handle to a region that can be used to specify the bounds of a hit test area. This parameter may be set to <b>NULL</b>.

### -param ptTest [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>


<a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that contains the coordinates of the point.

### -param pwHitTestCode [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a>*</b>

<b>WORD</b> that receives the hit test code that indicates whether the point in <i>ptTest</i> is in the background area bounded by <i>pRect</i> or <i>hrgn</i>. See <a href="/windows/desktop/Controls/theme-hit-test-retval">Hit Test Return Values</a> for a list of values returned.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The values in <i>ptTest</i> and <i>pRect</i> should be in the same coordinate system, such as client or screen. If the <i>hrgn</i> parameter is used, it must be specified in the same coordinates as <i>pRect</i> and <i>ptTest</i>.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>