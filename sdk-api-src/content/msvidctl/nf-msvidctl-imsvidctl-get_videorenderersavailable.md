---
UID: NF:msvidctl.IMSVidCtl.get_VideoRenderersAvailable
title: IMSVidCtl::get_VideoRenderersAvailable
author: windows-sdk-content
description: The get_VideoRenderersAvailable method retrieves a collection of video renderers available on the local system.
old-location: mstv\imsvidctl_get_videorenderersavailable.htm
old-project: mstv
ms.assetid: 20e5b2f3-33ea-4b0d-84b8-e4b0b61e0348
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_VideoRenderersAvailable method, IMSVidCtl.get_VideoRenderersAvailable, IMSVidCtl::get_VideoRenderersAvailable, IMSVidCtlget_VideoRenderersAvailable, get_VideoRenderersAvailable, get_VideoRenderersAvailable method [Microsoft TV Technologies], get_VideoRenderersAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_videorenderersavailable, msvidctl/IMSVidCtl::get_VideoRenderersAvailable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_VideoRenderersAvailable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::get_VideoRenderersAvailable


## -description


The <b>get_VideoRenderersAvailable</b> method retrieves a collection of video renderers available on the local system.


## -parameters




### -param pVal






#### - ppVal [out]

Receives an <a href="https://msdn.microsoft.com/cf8e1307-b4a5-464b-b9a6-32c195941309">IMSVidVideoRendererDevices</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method returns a collection of video renderer devices. Use the returned <a href="https://msdn.microsoft.com/cf8e1307-b4a5-464b-b9a6-32c195941309">IMSVidVideoRendererDevices</a> pointer to enumerate the collection.

<div class="alert"><b>Note</b>  In the current implementation, the collection always contains exactly one item: an <a href="https://msdn.microsoft.com/ffb9566f-1c03-4aba-a9ce-a47e42894ca0">MSVidVideoRenderer</a> object that represents the Video Mixing Renderer filter.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/0b69abaf-95ab-49b9-9555-a2244224cb5d">IMSVidCtl::get_VideoRendererActive</a>
 

 

