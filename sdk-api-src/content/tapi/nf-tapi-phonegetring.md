---
UID: NF:tapi.phoneGetRing
title: phoneGetRing function
author: windows-sdk-content
description: The phoneGetRing function enables an application to query the specified open phone device as to its current ring mode.
old-location: tapi2\phonegetring.htm
tech.root: TAPI
ms.assetid: 7ce96ce5-ab7c-42cf-8d06-e50e676ddbd2
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "_tapi2_phonegetring, phoneGetRing, phoneGetRing function [TAPI 2.2], tapi/phoneGetRing, tapi2.phonegetring"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneGetRing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# phoneGetRing function


## -description


The 
<b>phoneGetRing</b> function enables an application to query the specified open phone device as to its current ring mode.


## -parameters




### -param hPhone

Handle to the open phone device.


### -param lpdwRingMode

Ringing pattern with which the phone is ringing. Zero indicates that the phone is not ringing.


### -param lpdwVolume

Volume level with which the phone is ringing. This is a number in the range 0x00000000 (silence) to 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service provider-specific.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPHONESTATE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED.




## -remarks



The service provider defines the actual audible ringing patterns corresponding to each of the phone's ring modes.




## -see-also




<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

