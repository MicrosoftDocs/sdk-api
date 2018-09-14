---
UID: NF:tspi.TSPI_phoneSetRing
title: TSPI_phoneSetRing function
author: windows-sdk-content
description: The TSPI_phoneSetRing function rings the specified open phone device using the specified ring mode and volume.
old-location: tspi\tspi_phonesetring.htm
tech.root: TAPI
ms.assetid: 8540f39e-4891-48d9-a5b0-b928eeb4be0d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TSPI_phoneSetRing, TSPI_phoneSetRing function [TAPI 2.2], _tspi_tspi_phonesetring, tspi.tspi_phonesetring, tspi/TSPI_phoneSetRing
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tspi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneSetRing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_phoneSetRing function


## -description


The 
<b>TSPI_phoneSetRing</b> function rings the specified open phone device using the specified ring mode and volume.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdPhone

The handle to the phone to be rung.


### -param dwRingMode

The ringing pattern with which to ring the phone. This parameter must be within the range from zero through the value of the <b>dwNumRingModes</b> member in the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure. If <b>dwNumRingModes</b> is zero, the ring mode of the phone cannot be controlled; if <b>dwNumRingModes</b> is 1, a value of 0 for <i>dwRingMode</i> indicates that the phone should not be rung (silence), and other values from 1 through <b>dwNumRingModes</b> are valid ring modes for the phone device.


### -param dwVolume

The volume level with which the phone is to be rung. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service-provider specific. A value for <i>dwVolume</i> that is out of range is clamped by TAPI to the nearest value in range.


## -returns



Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALRINGMODE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.




## -remarks



The service provider defines the actual audible ringing patterns corresponding to each of the phone's ring modes.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/dcdfff60-e853-4ad7-a2b4-ddfc0ee73a48">TSPI_phoneGetRing</a>
 

 

