---
UID: NF:msvidctl.IMSVidCtl.DisableVideo
title: IMSVidCtl::DisableVideo
author: windows-sdk-content
description: The DisableVideo method disables the video renderer.
old-location: mstv\imsvidctl_disablevideo.htm
old-project: mstv
ms.assetid: 5c8f7af1-0416-4860-aa05-d2167452291e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DisableVideo, DisableVideo method [Microsoft TV Technologies], DisableVideo method [Microsoft TV Technologies],IMSVidCtl interface, IMSVidCtl interface [Microsoft TV Technologies],DisableVideo method, IMSVidCtl.DisableVideo, IMSVidCtl::DisableVideo, IMSVidCtlDisableVideo, mstv.imsvidctl_disablevideo, msvidctl/IMSVidCtl::DisableVideo
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msvidctl.h
api_name:
-	IMSVidCtl.DisableVideo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::DisableVideo


## -description


The <b>DisableVideo</b> method disables the video renderer.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method sets the active video renderer device to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/fb6e1db7-b980-4706-a1f1-cd6d8423bfb2">IMSVidCtl::put_VideoRendererActive</a>
 

 

