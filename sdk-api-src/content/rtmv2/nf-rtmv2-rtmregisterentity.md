---
UID: NF:rtmv2.RtmRegisterEntity
title: RtmRegisterEntity function (rtmv2.h)
description: The RtmRegisterEntity function registers a client with an instance of the routing table manager for a specific address family.
helpviewer_keywords: ["RtmRegisterEntity","RtmRegisterEntity function [RAS]","_rtmv2ref_rtmregisterentity","rras.rtmregisterentity","rtmv2/RtmRegisterEntity"]
old-location: rras\rtmregisterentity.htm
tech.root: RRAS
ms.assetid: 2b952ea2-cf33-49e3-ae31-a14b0907a1b5
ms.date: 12/05/2018
ms.keywords: RtmRegisterEntity, RtmRegisterEntity function [RAS], _rtmv2ref_rtmregisterentity, rras.rtmregisterentity, rtmv2/RtmRegisterEntity
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtmRegisterEntity
 - rtmv2/RtmRegisterEntity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmRegisterEntity
---

# RtmRegisterEntity function


## -description

The 
<b>RtmRegisterEntity</b> function registers a client with an instance of the routing table manager for a specific address family. The routing table manager returns a registration handle and a profile of the instance. The profile contains a list of values that are used when calling other functions. Values include the maximum number of destinations returned in a buffer by a single call.

Registration is the first action a client should take.

## -parameters

### -param RtmEntityInfo [in]

Pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_info">RTM_ENTITY_INFO</a> structure. This structure contains information that identifies the client to the routing table manager, such as the routing table manager instance and address family with which to register.

### -param ExportMethods [in]

Pointer to a <a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_export_methods">RTM_ENTITY_EXPORT_METHODS</a> structure that contains a list of methods exported by the client. This parameter is optional and can be set to <b>NULL</b> if the calling client has no methods to export.

### -param EventCallback [in]

A <b>RTM_EVENT_CALLBACK</b> structure that specifies the callback the routing table manager  uses to notify the client of events. The events are when a client registers and unregisters, when routes expire, and when changes to the best route to a destination have occurred. Only those changes specified when the client called 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>.

### -param ReserveOpaquePointer [in]

Specifies whether to reserve an opaque pointer in each destination for this instance of the protocol. Specify <b>TRUE</b> to reserve an opaque pointer in each destination. Specify <b>FALSE</b> to skip this action. These opaque pointers can be used to point to a private, protocol-specific context for each destination.

### -param RtmRegProfile [out]

On input, <i>RtmRegProfile</i> is a pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_regn_profile">RTM_REGN_PROFILE</a> structure. 




On output, <i>RtmRegProfile</i> is filled with the requested registration profile structure. The client must use the information returned in other function calls (information returned includes the number of equal-cost next hops and the maximum number of items returned by an enumeration function call).

### -param RtmRegHandle [out]

Receives a registration handle for the client. This handle must be used in all subsequent calls to the routing table manager.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified client has already registered with the routing table manager.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
Registry information for the routing table manager is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Registry information for the routing table manager was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains incorrect information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains incorrect information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
There are not enough available system resources to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to complete this operation.

</td>
</tr>
</table>

## -remarks

For sample code using this function, see 
<a href="/windows/desktop/RRAS/register-with-the-routing-table-manager">Register With the Routing Table Manager</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_export_methods">RTM_ENTITY_EXPORT_METHODS</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_info">RTM_ENTITY_INFO</a>



<a href="/windows/win32/api/rtmv2/nc-rtmv2-_event_callback">RTM_EVENT_CALLBACK</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_regn_profile">RTM_REGN_PROFILE</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmderegisterentity">RtmDeregisterEntity</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetregisteredentities">RtmGetRegisteredEntities</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseentities">RtmReleaseEntities</a>