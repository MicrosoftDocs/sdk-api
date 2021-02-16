---
UID: NC:routprot.PSTART_PROTOCOL
title: PSTART_PROTOCOL (routprot.h)
description: The StartProtocol function initializes the routing protocol's functionality.
helpviewer_keywords: ["PSTART_PROTOCOL","PSTART_PROTOCOL callback","StartProtocol","StartProtocol callback function [RAS]","_mpr_startprotocol","routprot/StartProtocol","rras.startprotocol"]
old-location: rras\startprotocol.htm
tech.root: RRAS
ms.assetid: 8c1c0173-5abf-4e44-a633-16742fd2a4c0
ms.date: 12/05/2018
ms.keywords: PSTART_PROTOCOL, PSTART_PROTOCOL callback, StartProtocol, StartProtocol callback function [RAS], _mpr_startprotocol, routprot/StartProtocol, rras.startprotocol
req.header: routprot.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSTART_PROTOCOL
 - routprot/PSTART_PROTOCOL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - StartProtocol
---

# PSTART_PROTOCOL callback function


## -description

The 
<b>StartProtocol</b> function initializes the routing protocol's functionality. The router manager uses this function to pass the routing protocol global configuration parameters and a set of API entry points. The protocol uses these entry points to call into the router manager.

## -parameters

### -param NotificationEvent [in]

Handle to an event object. The routing protocol signals this event when it wants the router manager to retrieve an asynchronous message from the queue maintained by the protocol.

### -param SupportFunctions [in]

Pointer to a 
<a href="/windows/desktop/api/routprot/ns-routprot-support_functions_50">SUPPORT_FUNCTIONS</a> structure. The fields of this structure are pointers to functions in the router manager. These functions allow the protocol to access information that spans routing protocols.

### -param GlobalInfo [in]

Pointer to protocol-defined global, as opposed to interface-specific, configuration information. This information is private to the routing protocol.

### -param StructureVersion [in]

Specifies the version of the information structures pointed to by the <i>GlobalInfo</i> parameter. In some cases, this is equal to the version of the routing protocol.

### -param StructureSize [in]

Specifies the size of each of the information structures pointed to by the <i>GlobalInfo</i> parameter. Since some information structures contain variable length members, the routing protocol isn't necessarily able to determine the size of the information from the version.

### -param StructureCount [in]

Specifies a count of the number of information structures pointed to by the <i>GlobalInfo</i> parameter. This parameter is always one.

## -returns

If the function succeeds, and the protocol is ready to receive interface information, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The attempt to initialize the routing protocol failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters pointed to by the <i>GlobalInfo</i> parameter is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pget_event_message">GetEventMessage</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>



<a href="/windows/desktop/api/routprot/ns-routprot-support_functions_50">SUPPORT_FUNCTIONS</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pstop_protocol">StopProtocol</a>