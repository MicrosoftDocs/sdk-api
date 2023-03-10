---
UID: NF:uxtheme.DrawThemeIcon
title: DrawThemeIcon function (uxtheme.h)
description: Draws an image from an image list with the icon effect defined by the visual style.
helpviewer_keywords: ["DrawThemeIcon","DrawThemeIcon function [Windows Controls]","controls.DrawThemeIcon","controls.inet_DrawThemeIcon","inet_DrawThemeIcon","inet_DrawThemeIcon_cpp","uxtheme/DrawThemeIcon"]
old-location: controls\DrawThemeIcon.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemeicon.htm
ms.date: 12/05/2018
ms.keywords: DrawThemeIcon, DrawThemeIcon function [Windows Controls], controls.DrawThemeIcon, controls.inet_DrawThemeIcon, inet_DrawThemeIcon, inet_DrawThemeIcon_cpp, uxtheme/DrawThemeIcon
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
 - DrawThemeIcon
 - uxtheme/DrawThemeIcon
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
 - DrawThemeIcon
---

# DrawThemeIcon function


## -description

Draws an image from an image list with the icon effect defined by the visual style.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part in which the image is drawn. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param pRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains, in logical coordinates, the rectangle in which the image is drawn.

### -param himl [in]

Type: <b>HIMAGELIST</b>

Handle to an <a href="/windows/desktop/api/commoncontrols/nn-commoncontrols-iimagelist">image list</a> that contains the image to draw.

### -param iImageIndex [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the index of the image to draw.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/commoncontrols/nn-commoncontrols-iimagelist">IImageList</a>



<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>



<b>Reference</b>