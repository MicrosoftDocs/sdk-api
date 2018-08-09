---
UID: NF:tspi.TSPI_phoneGetRing
title: TSPI_phoneGetRing function
author: windows-sdk-content
description: The TSPI_phoneGetRing function enables an application to query the specified open phone device as to its current ring mode.
old-location: tspi\tspi_phonegetring.htm
old-project: tapi
ms.assetid: dcdfff60-e853-4ad7-a2b4-ddfc0ee73a48
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_phoneGetRing, TSPI_phoneGetRing function [TAPI 2.2], _tspi_tspi_phonegetring, tspi.tspi_phonegetring, tspi/TSPI_phoneGetRing
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneGetRing
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_phoneGetRing function


## -description


The 
<b>TSPI_phoneGetRing</b> function enables an application to query the specified open phone device as to its current ring mode.


## -parameters




### -param hdPhone

The handle to the phone whose ring mode is to be queried.


### -param lpdwRingMode

The ringing pattern with which the phone is ringing. Zero indicates that the phone is not ringing.


### -param lpdwVolume

The volume level with which the phone is ringing. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service-provider specific.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.




## -remarks



The service provider defines the actual audible ringing patterns corresponding to each of phone's ring modes.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/8540f39e-4891-48d9-a5b0-b928eeb4be0d">TSPI_phoneSetRing</a>
 

 

