---
UID: NF:p2p.PeerPnrpUnregister
title: PeerPnrpUnregister function (p2p.h)
description: Deregisters a peer from a PNRP cloud.
helpviewer_keywords: ["PeerPnrpUnregister","PeerPnrpUnregister function [Peer Networking]","p2p.peerpnrpunregister","p2p/PeerPnrpUnregister"]
old-location: p2p\peerpnrpunregister.htm
tech.root: p2p
ms.assetid: ac032cfb-b1d4-4fe0-8d27-7d378aaa6aff
ms.date: 12/05/2018
ms.keywords: PeerPnrpUnregister, PeerPnrpUnregister function [Peer Networking], p2p.peerpnrpunregister, p2p/PeerPnrpUnregister
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
 - PeerPnrpUnregister
 - p2p/PeerPnrpUnregister
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
 - PeerPnrpUnregister
---

# PeerPnrpUnregister function


## -description

The <b>PeerPnrpUnregister</b> function deregisters a peer from a PNRP cloud.

## -parameters

### -param hRegistration [in]

Handle to a PNRP registration for the peer node obtained by a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpregister">PeerPnrpRegister</a>.

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

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpregister">PeerPnrpRegister</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpupdateregistration">PeerPnrpUpdateRegistration</a>