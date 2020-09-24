---
UID: NF:p2p.PeerPnrpUpdateRegistration
title: PeerPnrpUpdateRegistration function (p2p.h)
description: Updates the PNRP registration information for a name.
helpviewer_keywords: ["PeerPnrpUpdateRegistration","PeerPnrpUpdateRegistration function [Peer Networking]","p2p.peerpnrpupdateregistration","p2p/PeerPnrpUpdateRegistration"]
old-location: p2p\peerpnrpupdateregistration.htm
tech.root: p2p
ms.assetid: 628aa553-4a55-452b-bcca-4bb763fa6440
ms.date: 12/05/2018
ms.keywords: PeerPnrpUpdateRegistration, PeerPnrpUpdateRegistration function [Peer Networking], p2p.peerpnrpupdateregistration, p2p/PeerPnrpUpdateRegistration
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerPnrpUpdateRegistration
 - p2p/PeerPnrpUpdateRegistration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerPnrpUpdateRegistration
---

# PeerPnrpUpdateRegistration function


## -description

The <b>PeerPnrpUpdateRegistration</b> function updates the PNRP registration information for a name.

## -parameters

### -param hRegistration [in]

Handle to a PNRP registration for the peer node obtained by a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpregister">PeerPnrpRegister</a>.

### -param pRegistrationInfo [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_pnrp_registration_info">PEER_PNRP_REGISTRATION_INFO</a> structure that contains the endpoint information for the registering peer node.

## -returns

If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform the specified operation.

</td>
</tr>
</table>

## -remarks

The <b>pwzCloudName</b>  and <b>cAddresses</b> members of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_pnrp_registration_info">PEER_PNRP_REGISTRATION_INFO</a> provided in the <i>pRegistrationInfo</i> parameter cannot be changed with PeerPnrpUpdateRegistration. Attempting to do so will return an <b>E_INVALIDARG</b> error.

PeerPnrpUpdateRegistration has a maximum payload of 4k.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpregister">PeerPnrpRegister</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpunregister">PeerPnrpUnregister</a>