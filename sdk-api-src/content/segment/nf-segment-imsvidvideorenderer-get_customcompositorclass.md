---
UID: NF:segment.IMSVidVideoRenderer.get_CustomCompositorClass
title: IMSVidVideoRenderer::get_CustomCompositorClass
author: windows-sdk-content
description: The get_CustomCompositorClass method retrieves the class identifier (CLSID) of the Video Mixing Renderer's current image compositor, as a BSTR.
old-location: mstv\imsvidvideorenderer_get_customcompositorclass.htm
old-project: mstv
ms.assetid: d6ff1968-e891-432d-9271-f6d6a6a8a756
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_CustomCompositorClass method, IMSVidVideoRenderer.get_CustomCompositorClass, IMSVidVideoRenderer::get_CustomCompositorClass, IMSVidVideoRendererget_CustomCompositorClass, get_CustomCompositorClass, get_CustomCompositorClass method [Microsoft TV Technologies], get_CustomCompositorClass method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_customcompositorclass, segment/IMSVidVideoRenderer::get_CustomCompositorClass
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer.get_CustomCompositorClass
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVideoRenderer::get_CustomCompositorClass


## -description


The <b>get_CustomCompositorClass</b> method retrieves the class identifier (CLSID) of the Video Mixing Renderer's current image compositor, as a <b>BSTR</b>.


## -parameters




### -param CompositorCLSID






#### - pCompositorCLSID [out]

Receives a string representation of the CLSID.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is provided for Automation clients. C++ applications can use the <a href="https://msdn.microsoft.com/0ac48bbb-a0d3-4c37-9f3e-4f4cc79b550b">IMSVidVideoRenderer::get__CustomCompositorClass</a> method, which returns a <b>GUID</b> rather than a <b>BSTR</b>.

The caller must free the returned string, using the <b>SysFreeString</b> function.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/399a5151-b26a-4c33-9dd9-e7abb23cbd1c">IMSVidVideoRenderer::put_CustomCompositorClass</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

