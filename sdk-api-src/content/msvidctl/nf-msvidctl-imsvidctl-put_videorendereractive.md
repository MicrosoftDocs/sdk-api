---
UID: NF:msvidctl.IMSVidCtl.put_VideoRendererActive
title: IMSVidCtl::put_VideoRendererActive
author: windows-sdk-content
description: The put_VideoRendererActive method specifies the active video renderer.
old-location: mstv\imsvidctl_put_videorendereractive.htm
old-project: mstv
ms.assetid: fb6e1db7-b980-4706-a1f1-cd6d8423bfb2
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_VideoRendererActive method, IMSVidCtl.put_VideoRendererActive, IMSVidCtl::put_VideoRendererActive, IMSVidCtlput_VideoRendererActive, mstv.imsvidctl_put_videorendereractive, msvidctl/IMSVidCtl::put_VideoRendererActive, put_VideoRendererActive, put_VideoRendererActive method [Microsoft TV Technologies], put_VideoRendererActive method [Microsoft TV Technologies],IMSVidCtl interface
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msvidctl.h
api_name:
-	IMSVidCtl.put_VideoRendererActive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::put_VideoRendererActive


## -description


The <b>put_VideoRendererActive</b> method specifies the active video renderer.


## -parameters




### -param pVal [in]

Specifies a pointer to the <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a> interface of the video renderer device.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Currently the only supported video renderer is the Video Mixing Renderer (VMR) filter. The VMR is used by default, so it is not necessary to call this method.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/0b69abaf-95ab-49b9-9555-a2244224cb5d">IMSVidCtl::get_VideoRendererActive</a>
 

 

