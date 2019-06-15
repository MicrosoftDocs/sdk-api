---
UID: NF:strmif.IVMRImageCompositor.InitCompositionTarget
title: IVMRImageCompositor::InitCompositionTarget (strmif.h)
author: windows-sdk-content
description: The InitCompositionTarget method informs the compositor that a new composition target has been created.
old-location: dshow\ivmrimagecompositor_initcompositiontarget.htm
tech.root: DirectShow
ms.assetid: 16d54090-a0fa-480f-ba94-a15aa08d4576
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRImageCompositor interface [DirectShow],InitCompositionTarget method, IVMRImageCompositor.InitCompositionTarget, IVMRImageCompositor::InitCompositionTarget, IVMRImageCompositorInitCompositionTarget, InitCompositionTarget, InitCompositionTarget method [DirectShow], InitCompositionTarget method [DirectShow],IVMRImageCompositor interface, dshow.ivmrimagecompositor_initcompositiontarget, strmif/IVMRImageCompositor::InitCompositionTarget
ms.topic: method
f1_keywords: ["strmif/IVMRImageCompositor.InitCompositionTarget"]
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRImageCompositor.InitCompositionTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRImageCompositor::InitCompositionTarget


## -description



The <code>InitCompositionTarget</code> method informs the compositor that a new composition target has been created. The compositor should perform any necessary configuration work in this method. This could include attaching a Z or stencil buffer buffer for the new render target




## -parameters




### -param pD3DDevice [in]

Pointer to the <b>IUnknown</b> interface of the Direct3D device object.


### -param pddsRenderTarget [in]

Specifies the DirectDraw surface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

