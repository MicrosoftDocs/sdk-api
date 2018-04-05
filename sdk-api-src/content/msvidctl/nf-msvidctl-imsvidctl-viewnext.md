---
UID: NF:msvidctl.IMSVidCtl.ViewNext
title: IMSVidCtl::ViewNext method
author: windows-driver-content
description: The ViewNext method finds another input device to view the specified tune request.
old-location: mstv\imsvidctl_viewnext.htm
old-project: mstv
ms.assetid: 23b83339-f712-4b49-91f9-d0a1b02d64af
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidCtl, IMSVidCtl interface [Microsoft TV Technologies], ViewNext method, IMSVidCtl::ViewNext, IMSVidCtlViewNext, ViewNext method [Microsoft TV Technologies], ViewNext method [Microsoft TV Technologies], IMSVidCtl interface, ViewNext,IMSVidCtl.ViewNext, mstv.imsvidctl_viewnext, msvidctl/IMSVidCtl::ViewNext
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
-	IMSVidCtl.ViewNext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidCtl::ViewNext method


## -description


The <b>ViewNext</b> method finds another input device to view the specified tune request.

This method is supported only for analog tuner devices. It does not work with digital tuners.


## -parameters




### -param v






#### - pv [in]

Specifies the tune request as a <b>VARIANT</b> type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method works like the <a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">IMSVidCtl::View</a> method, with the following difference: If the system has more than one tuner that supports the specified network type, the <b>ViewNext</b> method skips the current input device and uses the next one. (The ordering of devices is arbitrary.)




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">IMSVidCtl::View</a>
 

 

