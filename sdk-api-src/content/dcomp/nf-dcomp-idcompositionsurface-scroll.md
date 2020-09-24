---
UID: NF:dcomp.IDCompositionSurface.Scroll
title: IDCompositionSurface::Scroll (dcomp.h)
description: Scrolls a rectangular area of a Microsoft DirectComposition logical surface.
helpviewer_keywords: ["IDCompositionSurface interface [DirectComposition]","Scroll method","IDCompositionSurface.Scroll","IDCompositionSurface::Scroll","Scroll","Scroll method [DirectComposition]","Scroll method [DirectComposition]","IDCompositionSurface interface","dcomp/IDCompositionSurface::Scroll","directcomp.idcompositionsurface_scroll"]
old-location: directcomp\idcompositionsurface_scroll.htm
tech.root: directcomp
ms.assetid: 0764C59A-DDDE-420C-B044-827B7EDC6CF1
ms.date: 12/05/2018
ms.keywords: IDCompositionSurface interface [DirectComposition],Scroll method, IDCompositionSurface.Scroll, IDCompositionSurface::Scroll, Scroll, Scroll method [DirectComposition], Scroll method [DirectComposition],IDCompositionSurface interface, dcomp/IDCompositionSurface::Scroll, directcomp.idcompositionsurface_scroll
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionSurface::Scroll
 - dcomp/IDCompositionSurface::Scroll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSurface.Scroll
---

# IDCompositionSurface::Scroll


## -description

Scrolls a rectangular area of a Microsoft DirectComposition logical surface.

## -parameters

### -param scrollRect [in]

The rectangular area of the surface to be scrolled, relative to the upper-left corner of the surface. If this parameter is NULL, the entire surface is scrolled.

### -param clipRect [in, optional]

The <i>clipRect</i> clips the destination (<i>scrollRect</i> after offset) of the scroll.
The only bitmap content that will be scrolled are those that remain inside the clip rectangle after the scroll is completed.

### -param offsetX [in]

The amount of horizontal scrolling, in pixels. Use positive values to scroll right, and negative values to scroll left.

### -param offsetY [in]

The amount of vertical scrolling, in pixels. Use positive values to scroll down, and negative values to scroll up.

## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method allows an application to blt/copy a sub-rectangle of a DirectComposition surface object. This avoids re-rendering content that is already available.  



The <i>scrollRect</i> rectangle must be contained in the boundaries of the surface.  If the <i>scrollRect</i> rectangle goes outside the bounds of the surface, this method fails.



The bits copied by the scroll operation (source) are defined by the intersection of the <i>scrollRect</i> and <i>clipRect</i> rectangles.  

The bits shown on the screen (destination) are defined by the intersection of the offset source rectangle and <i>clipRect</i>.



Scroll operations can only be called before calling <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">BeginDraw</a> or after calling <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-enddraw">EndDraw</a>.  Suspended or resumed surfaces are not candidates for scrolling because they are still being updated.



The application is responsible for ensuring that the scrollable area for an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvirtualsurface">IDCompositionVirtualSurface</a> is limited to valid pixels. The behavior for invalid pixels in the <i>scrollRect</i> is undefined.  

Virtual surface sub-rectangular areas that were discarded by a trim or a resize operation can't be scrolled even if the trim or resize is applied in the same batch.  <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim">Trim</a> and <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize">Resize</a> are applied immediately.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IDCompositionSurface</a>