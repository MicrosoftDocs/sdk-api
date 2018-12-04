---
UID: NF:rtmv2.RtmRegisterEntity
title: RtmRegisterEntity function
author: windows-sdk-content
description: The RtmRegisterEntity function registers a client with an instance of the routing table manager for a specific address family.
old-location: rras\rtmregisterentity.htm
tech.root: rras
ms.assetid: 2b952ea2-cf33-49e3-ae31-a14b0907a1b5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RtmRegisterEntity, RtmRegisterEntity function [RAS], _rtmv2ref_rtmregisterentity, rras.rtmregisterentity, rtmv2/RtmRegisterEntity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmRegisterEntity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmRegisterEntity function


## -description


The 
<b>RtmRegisterEntity</b> function registers a client with an instance of the routing table manager for a specific address family. The routing table manager returns a registration handle and a profile of the instance. The profile contains a list of values that are used when calling other functions. Values include the maximum number of destinations returned in a buffer by a single call.

Registration is the first action a client should take.


## -parameters




### -param RtmEntityInfo [in]

Pointer to an 
<a href="https://msdn.microsoft.com/b2a1e6b9-0cac-4316-98a0-ff1d44c5a15a">RTM_ENTITY_INFO</a> structure. This structure contains information that identifies the client to the routing table manager, such as the routing table manager instance and address family with which to register.


### -param ExportMethods [in]

Pointer to a <a href="https://msdn.microsoft.com/8198cfad-9188-4f49-92ab-1750ec16aec4">RTM_ENTITY_EXPORT_METHODS</a> structure that contains a list of methods exported by the client. This parameter is optional and can be set to <b>NULL</b> if the calling client has no methods to export.


### -param EventCallback [in]

A <b>RTM_EVENT_CALLBACK</b> structure that specifies the callback the routing table manager  uses to notify the client of events. The events are when a client registers and unregisters, when routes expire, and when changes to the best route to a destination have occurred. Only those changes specified when the client called 
<a href="https://msdn.microsoft.com/b6e04984-ac92-44a2-a18c-018c6b1b49a9">RtmRegisterForChangeNotification</a>.


### -param ReserveOpaquePointer [in]

Specifies whether to reserve an opaque pointer in each destination for this instance of the protocol. Specify <b>TRUE</b> to reserve an opaque pointer in each destination. Specify <b>FALSE</b> to skip this action. These opaque pointers can be used to point to a private, protocol-specific context for each destination.


### -param RtmRegProfile [out]

On input, <i>RtmRegProfile</i> is a pointer to an 
<a href="https://msdn.microsoft.com/26644a09-8d49-4c9f-a7cd-5edbf93e83d0">RTM_REGN_PROFILE</a> structure. 




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
<a href="https://msdn.microsoft.com/320cc97f-2875-4d26-b2f4-5611a43d5839">Register With the Routing Table Manager</a>.




## -see-also




<a href="https://msdn.microsoft.com/8198cfad-9188-4f49-92ab-1750ec16aec4">RTM_ENTITY_EXPORT_METHODS</a>



<a href="https://msdn.microsoft.com/b2a1e6b9-0cac-4316-98a0-ff1d44c5a15a">RTM_ENTITY_INFO</a>



<a href="https://msdn.microsoft.com/57179cea-d92b-4199-bb61-b34d980532cf">RTM_EVENT_CALLBACK</a>



<a href="https://msdn.microsoft.com/26644a09-8d49-4c9f-a7cd-5edbf93e83d0">RTM_REGN_PROFILE</a>



<a href="https://msdn.microsoft.com/dc13022b-e474-4442-a19c-856ee130c383">RtmDeregisterEntity</a>



<a href="https://msdn.microsoft.com/411e15bc-7f47-4ef7-9400-292203b581af">RtmGetRegisteredEntities</a>



<a href="https://msdn.microsoft.com/1f6c4275-0129-4f27-b9b2-bfda33d34d21">RtmReleaseEntities</a>
 

 

