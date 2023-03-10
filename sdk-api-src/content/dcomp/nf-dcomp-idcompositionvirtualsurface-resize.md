---
UID: NF:dcomp.IDCompositionVirtualSurface.Resize
title: IDCompositionVirtualSurface::Resize (dcomp.h)
description: Changes the logical size of this virtual surface object.
helpviewer_keywords: ["IDCompositionVirtualSurface interface [DirectComposition]","Resize method","IDCompositionVirtualSurface.Resize","IDCompositionVirtualSurface::Resize","Resize","Resize method [DirectComposition]","Resize method [DirectComposition]","IDCompositionVirtualSurface interface","dcomp/IDCompositionVirtualSurface::Resize","directcomp.idcompositionvirtualsurface_resize"]
old-location: directcomp\idcompositionvirtualsurface_resize.htm
tech.root: directcomp
ms.assetid: BB86CDA8-1DF0-436D-9FA3-95293E2B8C0E
ms.date: 12/05/2018
ms.keywords: IDCompositionVirtualSurface interface [DirectComposition],Resize method, IDCompositionVirtualSurface.Resize, IDCompositionVirtualSurface::Resize, Resize, Resize method [DirectComposition], Resize method [DirectComposition],IDCompositionVirtualSurface interface, dcomp/IDCompositionVirtualSurface::Resize, directcomp.idcompositionvirtualsurface_resize
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
 - IDCompositionVirtualSurface::Resize
 - dcomp/IDCompositionVirtualSurface::Resize
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
 - IDCompositionVirtualSurface.Resize
---

# IDCompositionVirtualSurface::Resize


## -description

Changes the logical size of this virtual surface object.

## -parameters

### -param width [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The new width of the virtual surface, in pixels. The maximum width is 16,777,216 pixels.

### -param height [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The new height of the virtual surface, in pixels. The maximum height is 16,777,216 pixels.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

When a virtual surface is resized, its contents are preserved up to the new boundaries of the surface. If the surface is made smaller, any previously allocated pixels that fall outside of the new width or height are discarded.

This method fails if <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> was called for this bitmap without a corresponding call to <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-enddraw">IDCompositionSurface::EndDraw</a>.

This method fails if <i>width</i> or <i>height</i> exceeds 16,777,216 pixels.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface">IDCompositionDevice::CreateVirtualSurface</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvirtualsurface">IDCompositionVirtualSurface</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim">IDCompositionVirtualSurface::Trim</a>