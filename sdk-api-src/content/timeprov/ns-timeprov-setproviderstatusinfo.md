---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SetProviderStatusInfo structure


## -description


A structure that is used by the 
<a href="https://msdn.microsoft.com/e52dd1d3-081a-4fcc-85d9-a1dcef0e8011">SetProviderStatusFunc</a> function.


## -struct-fields




### -field tpsCurrentState

The new state of the provider. This member can be one of the following values: 



					

<a id="TPC_Error"></a>
<a id="tpc_error"></a>
<a id="TPC_ERROR"></a>


#### TPC_Error

<a id="TPS_Running"></a>
<a id="tps_running"></a>
<a id="TPS_RUNNING"></a>


#### TPS_Running


### -field dwStratum

The new stratum of the provider. Computers using a hardware clock (such as cesium, GPS, or radio) to keep time are stratum 1. Computers that synchronize their time with another computer over the network are stratum N+1, where N is the stratum of the computer with which they are synchronizing.


### -field wszProvName

The name of the provider.


### -field hWaitEvent

A handle to an event to set to the signaled state when the operation has been completed. To create an event object, use the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function. 




If notification is not needed, this member can be <b>NULL</b>.


### -field pfnFree

A pointer to a 
<a href="https://msdn.microsoft.com/ea26aa92-af2a-4764-934d-2a21989a216f">SetProviderStatusInfoFreeFunc</a> function which frees the structure on completion.


### -field pHr

On completion, this member contains the result of the operation. If the operation succeeds, the result is S_OK. Otherwise, the result is one of the error codes defined in WinError.h.


### -field pdwSysStratum

On completion, this member contains the new system stratum. The system stratum is the lowest stratum of all time providers on the system. If the time provider with the lowest stratum increments its stratum, this increments the system stratum.


## -see-also




<a href="https://msdn.microsoft.com/e52dd1d3-081a-4fcc-85d9-a1dcef0e8011">SetProviderStatusFunc</a>



<a href="https://msdn.microsoft.com/ea26aa92-af2a-4764-934d-2a21989a216f">SetProviderStatusInfoFreeFunc</a>
 

 

