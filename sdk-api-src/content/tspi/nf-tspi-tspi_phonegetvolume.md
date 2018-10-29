---
UID: NF:tspi.TSPI_phoneGetVolume
title: TSPI_phoneGetVolume function
author: windows-sdk-content
description: The TSPI_phoneGetVolume function returns the volume setting of the specified phone's hookswitch device.
old-location: tspi\tspi_phonegetvolume.htm
tech.root: Tapi
ms.assetid: 4ea36cce-da68-47a3-ad79-4fc304a49451
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: TSPI_phoneGetVolume, TSPI_phoneGetVolume function [TAPI 2.2], _tspi_tspi_phonegetvolume, tspi.tspi_phonegetvolume, tspi/TSPI_phoneGetVolume
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
 - TSPI_phoneGetVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_phoneGetVolume function


## -description


The 
<b>TSPI_phoneGetVolume</b> function returns the volume setting of the specified phone's hookswitch device.


## -parameters




### -param hdPhone

The handle to the phone containing the hookswitch device whose volume setting is to be retrieved.


### -param dwHookSwitchDev

Identifies a single hookswitch device whose volume level is queried. This parameter uses one of the 
<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ constants</a>.


### -param lpdwVolume

A pointer to a <b>DWORD</b>-sized location into which the service provider writes the current volume setting of the hookswitch device. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service-provider specific.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/d929ed39-ba1d-4eae-9667-86d904ba96a8">TSPI_phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/c9aa2a3a-71ef-4214-b165-00a9620bb7e9">TSPI_phoneSetVolume</a>
 

 

