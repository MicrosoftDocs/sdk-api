---
UID: NF:p2p.PeerPnrpRegister
title: PeerPnrpRegister function (p2p.h)
description: Registers a peer with a PNRP cloud and returns a handle that can be used for registration updates.
helpviewer_keywords: ["PeerPnrpRegister","PeerPnrpRegister function [Peer Networking]","p2p.peerpnrpregister","p2p/PeerPnrpRegister"]
old-location: p2p\peerpnrpregister.htm
tech.root: p2p
ms.assetid: 18c26779-f50d-43bd-a772-763ceba25da8
ms.date: 12/05/2018
ms.keywords: PeerPnrpRegister, PeerPnrpRegister function [Peer Networking], p2p.peerpnrpregister, p2p/PeerPnrpRegister
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
 - PeerPnrpRegister
 - p2p/PeerPnrpRegister
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
 - PeerPnrpRegister
---

# PeerPnrpRegister function


## -description

The <b>PeerPnrpRegister</b> function registers a peer with a PNRP cloud and returns a handle that can be used for registration updates.
<div class="alert"><b>Note</b>  When called, this function will block until the PNRP service has been initiated.</div><div> </div>

## -parameters

### -param pcwzPeerName [in]

Pointer to a zero-terminated Unicode string that contains the peer name to register with the PNRP service.

### -param pRegistrationInfo [in, optional]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_pnrp_registration_info">PEER_PNRP_REGISTRATION_INFO</a> structure that contains the endpoint information for the registering peer node. If <b>NULL</b>, the API will register the peer with all known PNRP clouds, and any registered addresses are automatically selected by the infrastructure.

### -param phRegistration [out]

Handle to the  PNRP registration for the calling peer node. Use this handle to update the registration or to deregister with the PNRP service.

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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_IDENTITY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The local peer is using an identity that does not exist.

</td>
</tr>
</table>
 

Additionally, this function can return WSA values. For a complete list of possible values, see <a href="/windows/desktop/P2PSdk/pnrp-nsp-error-codes">PNRP NSP Error Codes</a>.

## -remarks

A  handle must be registered in a process separate of the process it will be resolved in. If a handle is registered and resolved within the same process it will not be recognized.

A name cannot be registered with an endpoint more than once. When updates to a registered name are required, use <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpupdateregistration">PeerPnrpUpdateRegistration</a>.

When <i>pRegistrationInfo</i> is <b>NULL</b>, or PEER_PNRP_AUTO_ADDRESSES is specified for <i>cAddresses</i>, the infrastructure will keep the addresses registered up to date as addresses change or cloud availability changes.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpunregister">PeerPnrpUnregister</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpupdateregistration">PeerPnrpUpdateRegistration</a>