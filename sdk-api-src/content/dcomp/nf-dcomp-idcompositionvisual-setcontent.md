---
UID: NF:dcomp.IDCompositionVisual.SetContent
title: IDCompositionVisual::SetContent
author: windows-sdk-content
description: Sets the Content property of this visual to the specified bitmap or window wrapper.
old-location: directcomp\idcompositionvisual_setcontent.htm
tech.root: directcomp
ms.assetid: 894E6E30-6C28-476D-9AE5-D0664A69E03C
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetContent method, IDCompositionVisual.SetContent, IDCompositionVisual::SetContent, SetContent, SetContent method [DirectComposition], SetContent method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetContent, directcomp.idcompositionvisual_setcontent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisual.SetContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual::SetContent


## -description


Sets the Content property of this visual to the specified bitmap or window wrapper.


## -parameters




### -param content [in, optional]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The object that is the new content of this visual. This parameter can be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The <i>content</i> parameter must point to one of the following:

<ul>
<li>An object that implements the <a href="https://msdn.microsoft.com/E271B4DC-5F09-426A-A5D3-43A48F30CB24">IDCompositionSurface</a> interface.</li>
<li>An object that implements the <b>IDXGISwapChain1</b> interface.</li>
<li>A wrapper object that is returned by the <a href="https://msdn.microsoft.com/391E98B4-9FFB-4065-91A4-99306B2FEB8F">CreateSurfaceFromHandle</a> or  <a href="https://msdn.microsoft.com/EA49F8EB-FAC8-421E-854D-C4AA81887EB0">CreateSurfaceFromHwnd</a> method.
</li>
</ul>
The new content replaces any content that was previously associated with the visual. If the <i>content</i> parameter is NULL, the visual has no associated content.

A visual can be associated with a bitmap object or a window wrapper. A bitmap is either a Microsoft DirectX swap chain or a Microsoft DirectComposition surface.

A window wrapper is created with the <a href="https://msdn.microsoft.com/EA49F8EB-FAC8-421E-854D-C4AA81887EB0">CreateSurfaceFromHwnd</a> method and is a stand-in for the rasterization of another window, which must be a top-level window or a layered child window. A window wrapper is conceptually equivalent to a bitmap that is the size of the target window on which the contents of the window are drawn. The contents include the target window's child windows (layered or otherwise), and any DirectComposition content that is drawn in the child windows. 

A DirectComposition surface wrapper is created with the <a href="https://msdn.microsoft.com/391E98B4-9FFB-4065-91A4-99306B2FEB8F">CreateSurfaceFromHandle</a> method and is a reference to a swap chain. An application might use a surface wrapper in a cross-process scenario where one process creates the swap chain and another process associates the bitmap with a visual.

The bitmap is always drawn at position (0,0) relative to the visual's coordinate system, although the coordinate system is directly affected by the OffsetX, OffsetY, and Transform properties, as well as indirectly by the transformations on ancestor visuals. The bitmap of a visual is always drawn behind the children of that visual.




## -see-also




<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>



<b>IDXGIFactory2::CreateSwapChain1</b>
 

 

