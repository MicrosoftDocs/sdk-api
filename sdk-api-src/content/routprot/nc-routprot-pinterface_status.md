---
UID: NC:routprot.PINTERFACE_STATUS
title: PINTERFACE_STATUS (routprot.h)
description: Router manager calls the InterfaceStatus function to change the status of an interface.
helpviewer_keywords: ["InterfaceStatus","InterfaceStatus callback function [RAS]","PINTERFACE_STATUS","PINTERFACE_STATUS callback","_mpr_interfacestatus","routprot/InterfaceStatus","rras.interfacestatus"]
old-location: rras\interfacestatus.htm
tech.root: RRAS
ms.assetid: 8fd674a6-375e-450c-bd6b-4f252977dd8e
ms.date: 12/05/2018
ms.keywords: InterfaceStatus, InterfaceStatus callback function [RAS], PINTERFACE_STATUS, PINTERFACE_STATUS callback, _mpr_interfacestatus, routprot/InterfaceStatus, rras.interfacestatus
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
 - PINTERFACE_STATUS
 - routprot/PINTERFACE_STATUS
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
 - InterfaceStatus
---

# PINTERFACE_STATUS callback function


## -description

Router manager calls the 
<b>InterfaceStatus</b> function to change the status of an interface.

The <a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">PINTERFACE_STATUS</a> type defines a pointer to this callback function. <i>InterfaceStatus</i> is a placeholder for the application-defined function name.

## -parameters

### -param InterfaceIndex [in]

Specifies the index of the interface to change.

### -param InterfaceActive [in]

Specifies whether the interface is active.

### -param StatusType [in]

Specifies the new interface status. This parameter is one of the following values. 




RIS_INTERFACE_ADDRESS_CHANGE

RIS_INTERFACE_ENABLED

RIS_INTERFACE_DISABLED

RIS_INTERFACE_MEDIA_PRESENT

RIS_INTERFACE_MEDIA_ABSENT

### -param StatusInfo [in]

Pointer to a structure that specifies information appropriate to the type of interface status type. For example, if the <i>StatusType</i> parameter specifies an address change, the <i>StatusInfo</i> parameter  points to a structure that contains the new address information, such as 
<a href="/windows/desktop/api/routprot/ns-routprot-ip_adapter_binding_info">IP_ADAPTER_BINDING_INFO</a>. This parameter may be <b>NULL</b>.

## -returns

If the function succeeds, the return value should be NO_ERROR.

If the function fails, the return value should be one of the following error codes.

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
Unspecified failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>InterfaceIndex</i> parameter is invalid (for example, no interface exists with that index).

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-padd_interface">AddInterface</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pdelete_interface">DeleteInterface</a>