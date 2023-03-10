---
UID: NF:dcomp.IDCompositionVirtualSurface.Trim
title: IDCompositionVirtualSurface::Trim (dcomp.h)
description: Discards pixels that fall outside of the specified trim rectangles.
helpviewer_keywords: ["IDCompositionVirtualSurface interface [DirectComposition]","Trim method","IDCompositionVirtualSurface.Trim","IDCompositionVirtualSurface::Trim","Trim","Trim method [DirectComposition]","Trim method [DirectComposition]","IDCompositionVirtualSurface interface","dcomp/IDCompositionVirtualSurface::Trim","directcomp.idcompositionvirtualsurface_trim"]
old-location: directcomp\idcompositionvirtualsurface_trim.htm
tech.root: directcomp
ms.assetid: 5A4F516F-B031-47E6-9A3D-068CF2C3D53A
ms.date: 12/05/2018
ms.keywords: IDCompositionVirtualSurface interface [DirectComposition],Trim method, IDCompositionVirtualSurface.Trim, IDCompositionVirtualSurface::Trim, Trim, Trim method [DirectComposition], Trim method [DirectComposition],IDCompositionVirtualSurface interface, dcomp/IDCompositionVirtualSurface::Trim, directcomp.idcompositionvirtualsurface_trim
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
 - IDCompositionVirtualSurface::Trim
 - dcomp/IDCompositionVirtualSurface::Trim
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
 - IDCompositionVirtualSurface.Trim
---

# IDCompositionVirtualSurface::Trim


## -description

Discards pixels that fall outside of the specified trim rectangles.

## -parameters

### -param rectangles [in, optional]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

An array of rectangles to keep.

### -param count [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of rectangles in the <i>rectangles</i> array.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A virtual surface might not  have enough storage for every pixel in the surface. An application instructs the composition engine to allocate memory for the surface by calling the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> method, and to release memory for the surface by calling the <b>IDCompositionVirtualSurface::Trim</b> method. The array of rectangles represents the regions of the virtual surface that should remain allocated after this method returns. Any pixels that are outside the specified set of rectangles are no longer used for texturing, and their memory may be reclaimed.



If the <i>count</i> parameter is zero, no pixels are kept, and all of the memory allocated for the virtual surface may be reclaimed. The <i>rectangles</i> parameter can be NULL only if the <i>count</i> parameter is zero.

This method fails if <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> was called for this bitmap without a corresponding call to <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-enddraw">IDCompositionSurface::EndDraw</a>.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface">IDCompositionDevice::CreateVirtualSurface</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvirtualsurface">IDCompositionVirtualSurface </a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize">IDCompositionVirtualSurface::Resize</a>