---
UID: NF:msvidctl.IMSVidCtl.get_OutputsActive
title: IMSVidCtl::get_OutputsActive
author: windows-driver-content
description: The get_OutputsActive method retrieves the output devices that are currently active.
old-location: mstv\imsvidctl_get_outputsactive.htm
old-project: mstv
ms.assetid: 9465ff38-c524-47e1-8bc0-bd6b2e0dea8c
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_OutputsActive method, IMSVidCtl.get_OutputsActive, IMSVidCtl::get_OutputsActive, IMSVidCtlget_OutputsActive, get_OutputsActive, get_OutputsActive method [Microsoft TV Technologies], get_OutputsActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_outputsactive, msvidctl/IMSVidCtl::get_OutputsActive
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
-	IMSVidCtl.get_OutputsActive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidCtl::get_OutputsActive


## -description


The <b>get_OutputsActive</b> method retrieves the output devices that are currently active.


## -parameters




### -param pVal






#### - ppVal [out]

Receives an <a href="https://msdn.microsoft.com/54776225-ad60-450b-99b4-851cae60ffa7">IMSVidOutputDevices</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/4ac78904-18ca-4bcb-9c0e-15595a756ecd">IMSVidCtl::get_AudioRendererActive</a>



<a href="https://msdn.microsoft.com/0b69abaf-95ab-49b9-9555-a2244224cb5d">IMSVidCtl::get_VideoRendererActive</a>
 

 

