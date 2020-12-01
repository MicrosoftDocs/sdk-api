---
UID: NC:routprot.PADD_INTERFACE
title: PADD_INTERFACE (routprot.h)
description: The AddInterface function adds an interface to be managed by the routing protocol.
helpviewer_keywords: ["AddInterface","AddInterface callback function [RAS]","DEMAND_DIAL","LOCAL_WORKSTATION_DIAL","PADD_INTERFACE","PADD_INTERFACE callback","PERMANENT","REMOTE_WORKSTATION_DIAL","_mpr_addinterface","routprot/AddInterface","rras.addinterface"]
old-location: rras\addinterface.htm
tech.root: RRAS
ms.assetid: d2a90d20-7a1f-4301-adab-76224a4f8310
ms.date: 12/05/2018
ms.keywords: AddInterface, AddInterface callback function [RAS], DEMAND_DIAL, LOCAL_WORKSTATION_DIAL, PADD_INTERFACE, PADD_INTERFACE callback, PERMANENT, REMOTE_WORKSTATION_DIAL, _mpr_addinterface, routprot/AddInterface, rras.addinterface
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
 - PADD_INTERFACE
 - routprot/PADD_INTERFACE
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
 - AddInterface
---

# PADD_INTERFACE callback function


## -description

The 
<b>AddInterface</b> function adds an interface to be managed by the routing protocol. The protocol should consider the interface to be in a disabled state. The router manager enables the interface by calling 
<a href="/windows/desktop/api/routprot/nc-routprot-pinterface_status">InterfaceStatus</a> with the RIS_INTERFACE_ENABLED flag.

When a user calls <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacetransportadd">MprAdminInterfaceTransportAdd</a>, the dynamic interface manager for the transport calls the router manager (for the transport) which calls this function for each of the routing protocols associated with that transport.

## -parameters

### -param InterfaceName [in]

Pointer to a Unicode string. The string contains a name that uniquely identifies the interface in the set of interfaces configured on the router.

### -param InterfaceIndex [in]

Specifies the interface in the set of interfaces configured on the router.

### -param InterfaceType [in]

Specifies the type of the interface. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERMANENT"></a><a id="permanent"></a><dl>
<dt><b>PERMANENT</b></dt>
</dl>
</td>
<td width="60%">
Permanent connectivity (for example, LAN, Frame Relay).

</td>
</tr>
<tr>
<td width="40%"><a id="DEMAND_DIAL"></a><a id="demand_dial"></a><dl>
<dt><b>DEMAND_DIAL</b></dt>
</dl>
</td>
<td width="60%">
Demand dial connectivity (analog, ISDN, PPTP, switched FR).

</td>
</tr>
<tr>
<td width="40%"><a id="LOCAL_WORKSTATION_DIAL"></a><a id="local_workstation_dial"></a><dl>
<dt><b>LOCAL_WORKSTATION_DIAL</b></dt>
</dl>
</td>
<td width="60%">
Local workstation connectivity only.

</td>
</tr>
<tr>
<td width="40%"><a id="REMOTE_WORKSTATION_DIAL"></a><a id="remote_workstation_dial"></a><dl>
<dt><b>REMOTE_WORKSTATION_DIAL</b></dt>
</dl>
</td>
<td width="60%">
Remote workstation connectivity only.

</td>
</tr>
</table>

### -param MediaType [in]

Reserved for future use.

### -param AccessType [in]

Reserved for future use.

### -param ConnectionType [in]

Reserved for future use.

### -param InterfaceInfo [in]

Pointer to a buffer that specifies protocol-defined configuration information associated with the interface. This information is private to the routing protocol.

### -param StructureVersion [in]

Specifies the version of the information structures pointed to by the <i>InterfaceInfo</i> parameter. In some cases, this is equal to the version of the routing protocol.

### -param StructureSize [in]

Specifies the size of each of the information structures pointed to by the <i>InterfaceInfo</i> parameter. Since some information structures contain variable length members, the routing protocol isn't necessarily able to determine the size of the information from the version.

### -param StructureCount [in]

Specifies a count of the number of information structures pointed to by the <i>InterfaceInfo</i> parameter. This parameter is always one.

## -returns

If the function succeeds, the return value is NO_ERROR.

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
The attempt to add the interface failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>InterfaceIndex</i> parameter is invalid (for example, an interface with that index already exists), or one of the parameters pointed to by <i>InterfaceInfo</i> is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pdelete_interface">DeleteInterface</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>