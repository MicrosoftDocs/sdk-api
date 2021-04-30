---
UID: NC:p2p.PFNPEER_VALIDATE_RECORD
title: PFNPEER_VALIDATE_RECORD (p2p.h)
description: The PFNPEER_VALIDATE_RECORD callback specifies the function that the Peer Graphing Infrastructure calls to validate records.
helpviewer_keywords: ["PFNPEER_VALIDATE_RECORD","PFNPEER_VALIDATE_RECORD callback","PFNPEER_VALIDATE_RECORD callback function [Peer Networking]","p2p.pfnpeer_validate_record","p2p/PFNPEER_VALIDATE_RECORD"]
old-location: p2p\pfnpeer_validate_record.htm
tech.root: p2p
ms.assetid: 5d81f09b-e46b-43e6-b0a8-ed7c236f2968
ms.date: 12/05/2018
ms.keywords: PFNPEER_VALIDATE_RECORD, PFNPEER_VALIDATE_RECORD callback, PFNPEER_VALIDATE_RECORD callback function [Peer Networking], p2p.pfnpeer_validate_record, p2p/PFNPEER_VALIDATE_RECORD
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
 - PFNPEER_VALIDATE_RECORD
 - p2p/PFNPEER_VALIDATE_RECORD
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
 - PFNPEER_VALIDATE_RECORD
---

# PFNPEER_VALIDATE_RECORD callback function


## -description

The <b>PFNPEER_VALIDATE_RECORD</b> callback specifies the function that the Peer Graphing Infrastructure calls     to validate records.

## -parameters

### -param hGraph [in]

Specifies the peer graph associated with the specified record.

### -param pvContext [in]

Pointer to the security context. This parameter should point to the <b>pvContext</b> member of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a> structure.

### -param pRecord [in]

Specifies the record to validate.

### -param changeType [in]

Specifies the reason the validation must occur.  Must be one of the  <a href="/windows/desktop/api/p2p/ne-p2p-peer_record_change_type">PEER_RECORD_CHANGE_TYPE</a> values.

## -returns

If this callback succeeds, the return value is S_OK; otherwise, the function returns one of the following errors:

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
<dt><b>PEER_E_DEFERRED_VALIDATION</b></dt>
</dl>
</td>
<td width="60%">
The specified record cannot be validated at this time because there is insufficient information to complete the operation. Validation is deferred. Call <a href="/windows/desktop/api/p2p/nf-p2p-peergraphvalidatedeferredrecords">PeerGraphValidateDeferredRecords</a> when sufficient information is obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_RECORD</b></dt>
</dl>
</td>
<td width="60%">
The specified record is invalid.

</td>
</tr>
</table>

## -remarks

When this callback is called by the Peer Graphing Infrastructure, a <a href="/windows/desktop/api/p2p/ne-p2p-peer_record_change_type">PEER_RECORD_CHANGE_TYPE</a> value is passed.  This specifies  the operation just performed on the record.  The application must verify the record based on the change type.  If the application  requires more information to verify the record, it can return PEER_E_DEFERRED_VALIDATION  and the Peer Graphing  Infrastructure places the record  in a deferred-record list.  Once the security mechanism has enough information to validate the record, it  calls <a href="/windows/desktop/api/p2p/nf-p2p-peergraphvalidatedeferredrecords">PeerGraphValidateDeferredRecords</a>, and any record in the deferred-record list is re-submitted for validation.

This callback can be invoked from any of the Peer Graphing API functions involving records, such as <a href="/windows/desktop/api/p2p/nf-p2p-peergraphupdaterecord">PeerGraphUpdateRecord</a>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a>



<a href="/windows/desktop/api/p2p/ne-p2p-peer_record_change_type">PEER_RECORD_CHANGE_TYPE</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphvalidatedeferredrecords">PeerGraphValidateDeferredRecords</a>