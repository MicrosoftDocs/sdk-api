---
UID: NF:tspi.TSPI_phoneSetVolume
title: TSPI_phoneSetVolume function
author: windows-sdk-content
description: The TSPI_phoneSetVolume function sets the volume of the speaker component of the specified hookswitch device to the specified level.
old-location: tspi\tspi_phonesetvolume.htm
tech.root: tapi
ms.assetid: c9aa2a3a-71ef-4214-b165-00a9620bb7e9
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_phoneSetVolume, TSPI_phoneSetVolume function [TAPI 2.2], _tspi_tspi_phonesetvolume, tspi.tspi_phonesetvolume, tspi/TSPI_phoneSetVolume
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
 - TSPI_phoneSetVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_phoneSetVolume function


## -description


The 
<b>TSPI_phoneSetVolume</b> function sets the volume of the speaker component of the specified hookswitch device to the specified level.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdPhone

The handle to the phone containing the speaker whose volume is to be set.


### -param dwHookSwitchDev

Identifies the hookswitch device whose speaker's volume is to be set. This parameter uses one of the 
<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ constants</a>.


### -param dwVolume

A <b>DWORD</b> specifying the new volume level of the hookswitch device. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service-provider specific. A value for <i>dwVolume</i> that is out of range is clamped by TAPI to the nearest value in range.


## -returns



Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.




## -remarks



None.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ Constants</a>



<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>
 

 

