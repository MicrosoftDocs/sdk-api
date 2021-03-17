---
UID: NS:timeprov.SetProviderStatusInfo
title: SetProviderStatusInfo (timeprov.h)
description: A structure that is used by the SetProviderStatusFunc function.
helpviewer_keywords: ["SetProviderStatusInfo","SetProviderStatusInfo structure","TPC_Error","TPS_Running","_win32_setproviderstatusinfo_str","base.setproviderstatusinfo_str","timeprov/SetProviderStatusInfo"]
old-location: base\setproviderstatusinfo_str.htm
tech.root: winprog
ms.assetid: 8e0a79ba-f76a-435a-9b0b-c3a2d9c390da
ms.date: 12/05/2018
ms.keywords: SetProviderStatusInfo, SetProviderStatusInfo structure, TPC_Error, TPS_Running, _win32_setproviderstatusinfo_str, base.setproviderstatusinfo_str, timeprov/SetProviderStatusInfo
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
targetos: Windows
req.typenames: SetProviderStatusInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetProviderStatusInfo
 - timeprov/SetProviderStatusInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Timeprov.h
api_name:
 - SetProviderStatusInfo
---

# SetProviderStatusInfo structure


## -description

A structure that is used by the 
<a href="/windows/desktop/api/timeprov/nc-timeprov-setproviderstatusfunc">SetProviderStatusFunc</a> function.

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
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function. 




If notification is not needed, this member can be <b>NULL</b>.

### -field pfnFree

A pointer to a 
<a href="/windows/desktop/api/timeprov/nc-timeprov-setproviderstatusinfofreefunc">SetProviderStatusInfoFreeFunc</a> function which frees the structure on completion.

### -field pHr

On completion, this member contains the result of the operation. If the operation succeeds, the result is S_OK. Otherwise, the result is one of the error codes defined in WinError.h.

### -field pdwSysStratum

On completion, this member contains the new system stratum. The system stratum is the lowest stratum of all time providers on the system. If the time provider with the lowest stratum increments its stratum, this increments the system stratum.

## -see-also

<a href="/windows/desktop/api/timeprov/nc-timeprov-setproviderstatusfunc">SetProviderStatusFunc</a>



<a href="/windows/desktop/api/timeprov/nc-timeprov-setproviderstatusinfofreefunc">SetProviderStatusInfoFreeFunc</a>