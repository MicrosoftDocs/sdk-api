---
UID: NF:stiusd.IStiUSD.RawWriteCommand
title: IStiUSD::RawWriteCommand method
author: windows-driver-content
description: A still image minidriver's IStiDevice::RawWriteCommand method sends command information to a still image device.
old-location: image\istiusd_rawwritecommand.htm
old-project: image
ms.assetid: c1b03ff5-1924-4221-b177-15214a8bf4f1
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IStiUSD, IStiUSD interface [Imaging Devices], RawWriteCommand method, IStiUSD::RawWriteCommand, RawWriteCommand method [Imaging Devices], RawWriteCommand method [Imaging Devices], IStiUSD interface, RawWriteCommand,IStiUSD.RawWriteCommand, image.istiusd_rawwritecommand, stifnc_508a67c1-4f4f-4324-bbb4-fc095fa023c4.xml, stiusd/IStiUSD::RawWriteCommand
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: stiusd.h
req.include-header: Stiusd.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	stiusd.h
api_name:
-	IStiUSD.RawWriteCommand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiUSD::RawWriteCommand method


## -description


A still image minidriver's <b>IStiDevice::RawWriteCommand</b> method sends command information to a still image device.


## -parameters




### -param lpBuffer

Caller-supplied pointer to a buffer containing data to be sent to the device.


### -param nNumberOfBytes

Caller-supplied number of bytes to be written. This is the number of bytes in the buffer pointed to by <i>lpBuffer</i>.


### -param lpOverlapped

Optional, caller-supplied pointer to an OVERLAPPED structure (described in the Microsoft Windows SDK documentation).


## -returns



If the operation succeeds, the method should return S_OK. Otherwise, it should return one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -remarks



It is only necessary to call <b>IStiUSD::RawWriteCommand</b> if commands and data are written to a device by different methods. For other devices, <a href="https://msdn.microsoft.com/library/windows/hardware/ff543839">IStiUSD::RawWriteData</a> can be used for both commands and data. If the call is not implemented, it must return STIERR_UNSUPPORTED.

Implementation of this method, along with the meaning of buffer contents, are vendor-defined.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543762">IStiDevice::RawWriteCommand</a>



<a href="https://msdn.microsoft.com/62740263-5bbb-48e1-be3d-9ee9cb37d6b9">IStiUSD</a>
 

 

