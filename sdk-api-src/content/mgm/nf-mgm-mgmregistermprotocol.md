---
UID: NF:mgm.MgmRegisterMProtocol
title: MgmRegisterMProtocol function (mgm.h)
description: The MgmRegisterMProtocol function is used by clients to register with the multicast group manager.
helpviewer_keywords: ["MgmRegisterMProtocol","MgmRegisterMProtocol function [RAS]","_mpr_mgmregistermprotocol","mgm/MgmRegisterMProtocol","rras.mgmregistermprotocol"]
old-location: rras\mgmregistermprotocol.htm
tech.root: RRAS
ms.assetid: a9b5f5f3-6e54-4a97-b3e7-e9e026947116
ms.date: 12/05/2018
ms.keywords: MgmRegisterMProtocol, MgmRegisterMProtocol function [RAS], _mpr_mgmregistermprotocol, mgm/MgmRegisterMProtocol, rras.mgmregistermprotocol
req.header: mgm.h
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
 - MgmRegisterMProtocol
 - mgm/MgmRegisterMProtocol
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
 - MgmRegisterMProtocol
---

# MgmRegisterMProtocol function


## -description

The 
<b>MgmRegisterMProtocol</b> function is used by clients to register with the multicast group manager. When the registration is complete, the multicast group manager returns a handle to the client. The client must supply this handle in subsequent MGM function calls.

## -parameters

### -param prpiInfo [in]

Pointer to a 
<a href="/windows/desktop/api/mgm/ns-mgm-routing_protocol_config">ROUTING_PROTOCOL_CONFIG</a> structure that contains pointers to callbacks into the client.

### -param dwProtocolId [in]

Specifies the ID of the client. The ID is unique for each client.

### -param dwComponentId [in]

Specifies the component ID for a specific instance of the client. This parameter is used with <i>dwProtocolId</i> to uniquely identify an instance of a client.

### -param phProtocol [out]

On input, the client must supply a pointer to a handle. 




On output, <i>phProtocol</i> receives the registration handle for the client. This handle must be used in subsequent calls to the multicast group manager.

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
Cannot register the specified client because an entry with the same protocol ID and component ID already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the call to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete this operation.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

Registering a protocol is the first operation any multicast routing protocol should perform. After registration, a routing protocol should take ownership of the appropriate interfaces before adding or deleting group memberships.

Only one routing protocol may take ownership of an interface at any given time. Multiple routing protocols may be registered with the multicast group manager, each protocol owning different interfaces.

## -see-also

<a href="/windows/desktop/api/mgm/nf-mgm-mgmderegistermprotocol">MgmDeRegisterMProtocol</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmtakeinterfaceownership">MgmTakeInterfaceOwnership</a>



<a href="/windows/desktop/api/mgm/ns-mgm-routing_protocol_config">ROUTING_PROTOCOL_CONFIG</a>