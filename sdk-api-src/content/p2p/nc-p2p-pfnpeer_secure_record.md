---
UID: NC:p2p.PFNPEER_SECURE_RECORD
title: PFNPEER_SECURE_RECORD (p2p.h)
description: The PFNPEER_SECURE_RECORD callback specifies the function that the Peer Graphing Infrastructure calls to secure records.
helpviewer_keywords: ["PFNPEER_SECURE_RECORD","PFNPEER_SECURE_RECORD callback","PFNPEER_SECURE_RECORD callback function [Peer Networking]","p2p.pfnpeer_secure_record","p2p/PFNPEER_SECURE_RECORD"]
old-location: p2p\pfnpeer_secure_record.htm
tech.root: p2p
ms.assetid: 454b40f6-a7de-4b59-ae35-a809c4510133
ms.date: 12/05/2018
ms.keywords: PFNPEER_SECURE_RECORD, PFNPEER_SECURE_RECORD callback, PFNPEER_SECURE_RECORD callback function [Peer Networking], p2p.pfnpeer_secure_record, p2p/PFNPEER_SECURE_RECORD
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
 - PFNPEER_SECURE_RECORD
 - p2p/PFNPEER_SECURE_RECORD
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
 - PFNPEER_SECURE_RECORD
---

# PFNPEER_SECURE_RECORD callback function


## -description

The <b>PFNPEER_SECURE_RECORD</b> callback specifies the function that the Peer Graphing Infrastructure calls     to secure records.

## -parameters

### -param hGraph [in]

Specifies the peer graph associated with the specified record.

### -param pvContext [in]

Pointer to the security context. This parameter  points to the <b>pvContext</b> member of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a> structure.

### -param pRecord [in]

Pointer to the record to secure.

### -param changeType [in]

Specifies the reason the validation must occur.     <a href="/windows/desktop/api/p2p/ne-p2p-peer_record_change_type">PEER_RECORD_CHANGE_TYPE</a> enumerates the valid values.

### -param ppSecurityData [out]

Specifies the security data for this record. This data is released by calling the method specified in the <b>pfnFreeSecurityData</b> member of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a> after the data is copied and added to the record.

## -returns

If this callback succeeds, the return value is S_OK.

## -remarks

This callback is invoked whenever an application calls any of the methods that modify records, such as <a href="/windows/desktop/api/p2p/nf-p2p-peergraphaddrecord">PeerGraphAddRecord</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphupdaterecord">PeerGraphUpdateRecord</a>. This callback  
should create  data that is specific to this record, such as a small digital signature, and return it through the <i>ppSecurityData</i> parameter.
This data is then  added to the record in the <b>securityData</b> member, and is  verified by the method specified by the <b>pfnValidateRecord</b> member of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a>.

<div class="alert"><b>Note</b>  This process happens on the local computer as well as any peer connected to the graph when the peer receives the record.</div>
<div> </div>
 If the operation specified by the <i>changeType</i> parameter is not allowed, the callback should return a failure code, such as PEER_E_NOT_AUTHORIZED,  instead of S_OK.

This callback can be invoked from any of the Peer Graphing API functions involving records, such as <a href="/windows/desktop/api/p2p/nf-p2p-peergraphupdaterecord">PeerGraphUpdateRecord</a>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a>



<a href="/windows/desktop/api/p2p/ne-p2p-peer_record_change_type">PEER_RECORD_CHANGE_TYPE</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a>
