---
UID: NF:mgm.MgmTakeInterfaceOwnership
title: MgmTakeInterfaceOwnership function (mgm.h)
description: The MgmTakeInterfaceOwnership function is called by a client (such as a routing protocol) when it is enabled on an interface.
helpviewer_keywords: ["MgmTakeInterfaceOwnership","MgmTakeInterfaceOwnership function [RAS]","_mpr_mgmtakeinterfaceownership","mgm/MgmTakeInterfaceOwnership","rras.mgmtakeinterfaceownership"]
old-location: rras\mgmtakeinterfaceownership.htm
tech.root: RRAS
ms.assetid: b072c884-0b84-4dd9-a14c-185f5d327017
ms.date: 12/05/2018
ms.keywords: MgmTakeInterfaceOwnership, MgmTakeInterfaceOwnership function [RAS], _mpr_mgmtakeinterfaceownership, mgm/MgmTakeInterfaceOwnership, rras.mgmtakeinterfaceownership
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
 - MgmTakeInterfaceOwnership
 - mgm/MgmTakeInterfaceOwnership
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
 - MgmTakeInterfaceOwnership
---

# MgmTakeInterfaceOwnership function


## -description

The 
<b>MgmTakeInterfaceOwnership</b> function is called by a client (such as a routing protocol) when it is enabled on an interface.

Only one client can take ownership of a given interface at any time. The only exception to this rule is the IGMP. IGMP can coexist with another client on an interface.

## -parameters

### -param hProtocol [in]

Handle to the protocol obtained from a previous call to 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmregistermprotocol">MgmRegisterMProtocol</a>.

### -param dwIfIndex [in]

Specifies the index of the interface of which to take ownership.

### -param dwIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.

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
The specified interface is already owned by another routing protocol.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid handle to a client.

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

A client must take ownership of an interface only after registering itself with the multicast group manager, but before it adds group membership entries.

## -see-also

<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetprotocoloninterface">MgmGetProtocolOnInterface</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmregistermprotocol">MgmRegisterMProtocol</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmreleaseinterfaceownership">MgmReleaseInterfaceOwnership</a>