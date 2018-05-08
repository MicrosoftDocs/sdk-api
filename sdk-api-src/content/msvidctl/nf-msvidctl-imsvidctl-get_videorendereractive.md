---
UID: NF:msvidctl.IMSVidCtl.get_VideoRendererActive
title: IMSVidCtl::get_VideoRendererActive
author: windows-driver-content
description: The get_VideoRendererActive method retrieves the currently active video renderer.
old-location: mstv\imsvidctl_get_videorendereractive.htm
old-project: mstv
ms.assetid: 0b69abaf-95ab-49b9-9555-a2244224cb5d
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_VideoRendererActive method, IMSVidCtl.get_VideoRendererActive, IMSVidCtl::get_VideoRendererActive, IMSVidCtlget_VideoRendererActive, get_VideoRendererActive, get_VideoRendererActive method [Microsoft TV Technologies], get_VideoRendererActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_videorendereractive, msvidctl/IMSVidCtl::get_VideoRendererActive
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msvidctl.h
api_name:
-	IMSVidCtl.get_VideoRendererActive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidCtl::get_VideoRendererActive


## -description


The <b>get_VideoRendererActive</b> method retrieves the currently active video renderer.


## -parameters




### -param pVal






#### - ppVal [out]

Receives an <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a> interface pointer.  The caller must release the interface. If no video renderer is active, this parameter receives the value <b>NULL</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/fb6e1db7-b980-4706-a1f1-cd6d8423bfb2">IMSVidCtl::put_VideoRendererActive</a>
 

 

