---
UID: NS:timeprov.SetProviderStatusInfo
title: SetProviderStatusInfo
author: windows-sdk-content
description: A structure that is used by the SetProviderStatusFunc function.
old-location: base\setproviderstatusinfo_str.htm
tech.root: sysinfo
ms.assetid: 8e0a79ba-f76a-435a-9b0b-c3a2d9c390da
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: SetProviderStatusInfo, SetProviderStatusInfo structure, TPC_Error, TPS_Running, _win32_setproviderstatusinfo_str, base.setproviderstatusinfo_str, timeprov/SetProviderStatusInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: timeprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - HeaderDef
api_location:
 - Timeprov.h
api_name:
 - SetProviderStatusInfo
product: Windows
targetos: Windows
req.typenames: SetProviderStatusInfo
req.redist: 
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
 

 

