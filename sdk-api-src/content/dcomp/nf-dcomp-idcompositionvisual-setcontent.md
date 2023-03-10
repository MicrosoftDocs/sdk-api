---
UID: NF:dcomp.IDCompositionVisual.SetContent
title: IDCompositionVisual::SetContent (dcomp.h)
description: Sets the Content property of this visual to the specified bitmap or window wrapper.
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","SetContent method","IDCompositionVisual.SetContent","IDCompositionVisual::SetContent","SetContent","SetContent method [DirectComposition]","SetContent method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::SetContent","directcomp.idcompositionvisual_setcontent"]
old-location: directcomp\idcompositionvisual_setcontent.htm
tech.root: directcomp
ms.assetid: 894E6E30-6C28-476D-9AE5-D0664A69E03C
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetContent method, IDCompositionVisual.SetContent, IDCompositionVisual::SetContent, SetContent, SetContent method [DirectComposition], SetContent method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetContent, directcomp.idcompositionvisual_setcontent
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
 - IDCompositionVisual::SetContent
 - dcomp/IDCompositionVisual::SetContent
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
 - IDCompositionVisual.SetContent
---

# IDCompositionVisual::SetContent


## -description

Sets the Content property of this visual to the specified bitmap or window wrapper.

## -parameters

### -param content [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The object that is the new content of this visual. This parameter can be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

The <i>content</i> parameter must point to one of the following:

<ul>
<li>An object that implements the <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IDCompositionSurface</a> interface.</li>
<li>An object that implements the <b>IDXGISwapChain1</b> interface.</li>
<li>A wrapper object that is returned by the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurfacefromhandle">CreateSurfaceFromHandle</a> or  <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurfacefromhwnd">CreateSurfaceFromHwnd</a> method.
</li>
</ul>
The new content replaces any content that was previously associated with the visual. If the <i>content</i> parameter is NULL, the visual has no associated content.

A visual can be associated with a bitmap object or a window wrapper. A bitmap is either a Microsoft DirectX swap chain or a Microsoft DirectComposition surface.

A window wrapper is created with the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurfacefromhwnd">CreateSurfaceFromHwnd</a> method and is a stand-in for the rasterization of another window, which must be a top-level window or a layered child window. A window wrapper is conceptually equivalent to a bitmap that is the size of the target window on which the contents of the window are drawn. The contents include the target window's child windows (layered or otherwise), and any DirectComposition content that is drawn in the child windows. 

A DirectComposition surface wrapper is created with the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurfacefromhandle">CreateSurfaceFromHandle</a> method and is a reference to a swap chain. An application might use a surface wrapper in a cross-process scenario where one process creates the swap chain and another process associates the bitmap with a visual.

The bitmap is always drawn at position (0,0) relative to the visual's coordinate system, although the coordinate system is directly affected by the OffsetX, OffsetY, and Transform properties, as well as indirectly by the transformations on ancestor visuals. The bitmap of a visual is always drawn behind the children of that visual.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>



<b>IDXGIFactory2::CreateSwapChain1</b>