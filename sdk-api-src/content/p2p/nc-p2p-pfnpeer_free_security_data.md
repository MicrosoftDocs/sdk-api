---
UID: NC:p2p.PFNPEER_FREE_SECURITY_DATA
title: PFNPEER_FREE_SECURITY_DATA (p2p.h)
description: The PFNPEER_FREE_SECURITY_DATA callback specifies the function that the Peer Graphing Infrastructure calls to free data returned by PFNPEER_SECURE_RECORD and PFNPEER_VALIDATE_RECORD callbacks.
helpviewer_keywords: ["PFNPEER_FREE_SECURITY_DATA","PFNPEER_FREE_SECURITY_DATA callback","PFNPEER_FREE_SECURITY_DATA callback function [Peer Networking]","p2p.pfnpeer_free_security_data","p2p/PFNPEER_FREE_SECURITY_DATA"]
old-location: p2p\pfnpeer_free_security_data.htm
tech.root: p2p
ms.assetid: aa340e32-6d7f-4218-b120-8c352fdbda0f
ms.date: 12/05/2018
ms.keywords: PFNPEER_FREE_SECURITY_DATA, PFNPEER_FREE_SECURITY_DATA callback, PFNPEER_FREE_SECURITY_DATA callback function [Peer Networking], p2p.pfnpeer_free_security_data, p2p/PFNPEER_FREE_SECURITY_DATA
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
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
 - PFNPEER_FREE_SECURITY_DATA
 - p2p/PFNPEER_FREE_SECURITY_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - P2P.h
api_name:
 - PFNPEER_FREE_SECURITY_DATA
---

# PFNPEER_FREE_SECURITY_DATA callback function


## -description

The <b>PFNPEER_FREE_SECURITY_DATA</b> callback specifies the function that the Peer Graphing Infrastructure calls     to free data returned by <a href="/windows/desktop/api/p2p/nc-p2p-pfnpeer_secure_record">PFNPEER_SECURE_RECORD</a> and <a href="/windows/desktop/api/p2p/nc-p2p-pfnpeer_validate_record">PFNPEER_VALIDATE_RECORD</a>  callbacks.

## -parameters

### -param hGraph [in]

Specifies the peer graph associated with the specified record.

### -param pvContext [in]

Pointer to the security context to free. This  parameter is set to the value of the <b>pvContext</b> member of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a> structure passed in <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>.

### -param pSecurityData [in]

Pointer to the security data to  free.

## -returns

If the callback is successful, the return value is S_OK. Otherwise, the callback   returns one of the following values.

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

This callback can be invoked from any of the Peer Graphing API functions involving records, such as <a href="/windows/desktop/api/p2p/nf-p2p-peergraphupdaterecord">PeerGraphUpdateRecord</a>.

## -see-also

[PEER_DATA](./ns-p2p-peer_data.md)



<a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>