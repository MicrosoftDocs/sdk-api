---
UID: NF:msvidctl.IMSVidCtl.get_AudioRenderersAvailable
title: IMSVidCtl::get_AudioRenderersAvailable
author: windows-sdk-content
description: The get_AudioRenderersAvailable method retrieves the available audio renderers.
old-location: mstv\imsvidctl_get_audiorenderersavailable.htm
tech.root: mstv
ms.assetid: 6ab81536-2701-408e-be3a-f44375ef8193
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_AudioRenderersAvailable method, IMSVidCtl.get_AudioRenderersAvailable, IMSVidCtl::get_AudioRenderersAvailable, IMSVidCtlget_AudioRenderersAvailable, get_AudioRenderersAvailable, get_AudioRenderersAvailable method [Microsoft TV Technologies], get_AudioRenderersAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_audiorenderersavailable, msvidctl/IMSVidCtl::get_AudioRenderersAvailable
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_AudioRenderersAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::get_AudioRenderersAvailable


## -description


The <b>get_AudioRenderersAvailable</b> method retrieves the available audio renderers.


## -parameters




### -param pVal

TBD




#### - ppVal [out]

Receives an <a href="https://msdn.microsoft.com/2cf03260-7abe-4602-8364-447d076a4f76">IMSVidAudioRendererDevices</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method returns a read-only collection of input devices. Use the returned <a href="https://msdn.microsoft.com/2cf03260-7abe-4602-8364-447d076a4f76">IMSVidAudioRendererDevices</a> pointer to enumerate the collection.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/4ac78904-18ca-4bcb-9c0e-15595a756ecd">IMSVidCtl::get_AudioRendererActive</a>
 

 

