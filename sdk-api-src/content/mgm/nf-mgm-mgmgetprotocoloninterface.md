---
UID: NF:mgm.MgmGetProtocolOnInterface
title: MgmGetProtocolOnInterface function (mgm.h)
description: The MgmGetProtocolOnInterface function retrieves the protocol ID of the multicast routing protocol that owns the specified interface.
helpviewer_keywords: ["MgmGetProtocolOnInterface","MgmGetProtocolOnInterface function [RAS]","_mpr_mgmgetprotocoloninterface","mgm/MgmGetProtocolOnInterface","rras.mgmgetprotocoloninterface"]
old-location: rras\mgmgetprotocoloninterface.htm
tech.root: RRAS
ms.assetid: 38f6cc9b-ae9e-49a3-8f5e-835699ff3d60
ms.date: 12/05/2018
ms.keywords: MgmGetProtocolOnInterface, MgmGetProtocolOnInterface function [RAS], _mpr_mgmgetprotocoloninterface, mgm/MgmGetProtocolOnInterface, rras.mgmgetprotocoloninterface
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
 - MgmGetProtocolOnInterface
 - mgm/MgmGetProtocolOnInterface
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
 - MgmGetProtocolOnInterface
---

# MgmGetProtocolOnInterface function


## -description

The 
<b>MgmGetProtocolOnInterface</b> function retrieves the protocol ID of the multicast routing protocol that owns the specified interface.

## -parameters

### -param dwIfIndex [in]

Specifies the index of the interface for which to retrieve the protocol ID.

### -param dwIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.

### -param pdwIfProtocolId [in, out]

On input, the client must supply a pointer to a <b>DWORD</b>-sized memory location. 




On output, <i>pdwIfProtocolId</i> receives the ID of the protocol on the interface specified by <i>dwIfIndex</i>.

### -param pdwIfComponentId [in, out]

On input, the client must supply a pointer to a <b>DWORD</b> value. 




On output, <i>pdwIfComponentId</i> receives the component ID for the instance of the protocol on the interface. This parameter is used with <i>pdwIfProtocolId</i> to uniquely identify an instance of a routing protocol.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface was not found by the multicast group manager.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/mgm/nf-mgm-mgmreleaseinterfaceownership">MgmReleaseInterfaceOwnership</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmtakeinterfaceownership">MgmTakeInterfaceOwnership</a>