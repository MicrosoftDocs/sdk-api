---
UID: NF:strmif.IVMRImageCompositor.TermCompositionTarget
title: IVMRImageCompositor::TermCompositionTarget (strmif.h)
author: windows-sdk-content
description: The TermCompositionTarget method informs the compositor that the current composition target is being replaced. Compositors should perform any necessary cleanup of the composition target in this method.
old-location: dshow\ivmrimagecompositor_termcompositiontarget.htm
tech.root: DirectShow
ms.assetid: a9526be0-06aa-4fe3-ba05-fbac01806ec4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRImageCompositor interface [DirectShow],TermCompositionTarget method, IVMRImageCompositor.TermCompositionTarget, IVMRImageCompositor::TermCompositionTarget, IVMRImageCompositorStopCompositing, TermCompositionTarget, TermCompositionTarget method [DirectShow], TermCompositionTarget method [DirectShow],IVMRImageCompositor interface, dshow.ivmrimagecompositor_termcompositiontarget, strmif/IVMRImageCompositor::TermCompositionTarget
ms.topic: method
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
 - IVMRImageCompositor.TermCompositionTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRImageCompositor::TermCompositionTarget


## -description



The <code>TermCompositionTarget</code> method informs the compositor that the current composition target is being replaced. Compositors should perform any necessary cleanup of the composition target in this method.




## -parameters




### -param pD3DDevice [in]

Pointer to the <b>IUnknown</b> interface of the Direct3D device object.


### -param pddsRenderTarget [in]

Specifies the DirectDraw surface


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/d905e871-c156-4140-bb3f-a19fa0cd79be">IVMRImageCompositor Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

