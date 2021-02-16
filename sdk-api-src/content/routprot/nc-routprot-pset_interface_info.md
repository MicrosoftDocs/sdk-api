---
UID: NC:routprot.PSET_INTERFACE_INFO
title: PSET_INTERFACE_INFO (routprot.h)
description: The SetInterfaceInfo function sets the configuration of a specific interface managed by the routing protocol.
helpviewer_keywords: ["PSET_INTERFACE_INFO","PSET_INTERFACE_INFO callback","SetInterfaceInfo","SetInterfaceInfo callback function [RAS]","_mpr_setinterfaceinfo","routprot/SetInterfaceInfo","rras.setinterfaceinfo"]
old-location: rras\setinterfaceinfo.htm
tech.root: RRAS
ms.assetid: abcfa220-a860-48cc-92c5-60ce655678b7
ms.date: 12/05/2018
ms.keywords: PSET_INTERFACE_INFO, PSET_INTERFACE_INFO callback, SetInterfaceInfo, SetInterfaceInfo callback function [RAS], _mpr_setinterfaceinfo, routprot/SetInterfaceInfo, rras.setinterfaceinfo
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
 - PSET_INTERFACE_INFO
 - routprot/PSET_INTERFACE_INFO
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
 - SetInterfaceInfo
---

# PSET_INTERFACE_INFO callback function


## -description

The 
<b>SetInterfaceInfo</b> function sets the configuration of a specific interface managed by the routing protocol.

## -parameters

### -param InterfaceIndex [in]

Specifies the interface in the set of interfaces configured on the router.

### -param InterfaceInfo [in]

Pointer to a buffer that holds the protocol-defined configuration information associated with the interface. This information is private to the routing protocol.

### -param StructureVersion [in]

Specifies the version of the information structures pointed to by the <i>InterfaceInfo</i> parameter. In some cases, this is equal to the version of the routing protocol.

### -param StructureSize [in]

Specifies the size of each of the information structures pointed to by the <i>InterfaceInfo</i> parameter. Since some information structures contain variable length members, the routing protocol is not necessarily able to determine the size of the information from the version.

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
The attempt to set the interface configuration failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>InterfaceIndex</i> parameter is invalid (for example, no interface exists with that index), the <i>InterfaceInfo</i> parameter is <b>NULL</b>, or one of the parameters in the configuration information is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pget_interface_info">GetInterfaceInfo</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>