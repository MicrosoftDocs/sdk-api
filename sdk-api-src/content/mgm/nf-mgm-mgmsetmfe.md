---
UID: NF:mgm.MgmSetMfe
title: MgmSetMfe function (mgm.h)
description: The MgmSetMfe function changes the upstream neighbor for an MFE. An MFE contains the information about which interface is receiving and which interfaces are forwarding multicast data.
helpviewer_keywords: ["MgmSetMfe","MgmSetMfe function [RAS]","_mpr_mgmsetmfe","mgm/MgmSetMfe","rras.mgmsetmfe"]
old-location: rras\mgmsetmfe.htm
tech.root: RRAS
ms.assetid: 143c080a-be80-47fb-a159-e6c95aa0d7ea
ms.date: 12/05/2018
ms.keywords: MgmSetMfe, MgmSetMfe function [RAS], _mpr_mgmsetmfe, mgm/MgmSetMfe, rras.mgmsetmfe
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MgmSetMfe
 - mgm/MgmSetMfe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mgm.h
api_name:
 - MgmSetMfe
---

# MgmSetMfe function


## -description

The 
<b>MgmSetMfe</b> function changes the upstream neighbor for an MFE. An MFE contains the information about which interface is receiving and which interfaces are forwarding multicast data.

## -parameters

### -param hProtocol [in]

Handle to the protocol obtained from a previous call to 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmregistermprotocol">MgmRegisterMProtocol</a>.

### -param pmimm [in]

Pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a> structure that specifies the MFE to change. Specify the new neighbor in the <b>dwUpstreamNeighbor</b> member.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified MFE was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a>