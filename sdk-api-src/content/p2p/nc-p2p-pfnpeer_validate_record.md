---
UID: NC:p2p.PFNPEER_VALIDATE_RECORD
title: PFNPEER_VALIDATE_RECORD
author: windows-sdk-content
description: The PFNPEER_VALIDATE_RECORD callback specifies the function that the Peer Graphing Infrastructure calls to validate records.
old-location: p2p\pfnpeer_validate_record.htm
old-project: p2psdk
ms.assetid: 5d81f09b-e46b-43e6-b0a8-ed7c236f2968
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PFNPEER_VALIDATE_RECORD, PFNPEER_VALIDATE_RECORD callback, PFNPEER_VALIDATE_RECORD callback function [Peer Networking], p2p.pfnpeer_validate_record, p2p/PFNPEER_VALIDATE_RECORD
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: p2p.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: OPM_STANDARD_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - P2P.h
api_name:
 - PFNPEER_VALIDATE_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PFNPEER_VALIDATE_RECORD callback function


## -description


The <b>PFNPEER_VALIDATE_RECORD</b> callback specifies the function that the Peer Graphing Infrastructure calls     to validate records.


## -parameters




### -param hGraph [in]

Specifies the peer graph associated with the specified record.


### -param pvContext [in]

Pointer to the security context. This parameter should point to the <b>pvContext</b> member of the <a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a> structure.


### -param pRecord [in]

Specifies the record to validate.


### -param changeType [in]

Specifies the reason the validation must occur.  Must be one of the  <a href="https://msdn.microsoft.com/d2451b45-eb42-4401-ab1d-505a41e25822">PEER_RECORD_CHANGE_TYPE</a> values.


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
The specified record cannot be validated at this time because there is insufficient information to complete the operation. Validation is deferred. Call <a href="https://msdn.microsoft.com/a9a48d8a-f31e-4526-bd09-826f04a564b1">PeerGraphValidateDeferredRecords</a> when sufficient information is obtained.

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



When this callback is called by the Peer Graphing Infrastructure, a <a href="https://msdn.microsoft.com/d2451b45-eb42-4401-ab1d-505a41e25822">PEER_RECORD_CHANGE_TYPE</a> value is passed.  This specifies  the operation just performed on the record.  The application must verify the record based on the change type.  If the application  requires more information to verify the record, it can return PEER_E_DEFERRED_VALIDATION  and the Peer Graphing  Infrastructure places the record  in a deferred-record list.  Once the security mechanism has enough information to validate the record, it  calls <a href="https://msdn.microsoft.com/a9a48d8a-f31e-4526-bd09-826f04a564b1">PeerGraphValidateDeferredRecords</a>, and any record in the deferred-record list is re-submitted for validation.

This callback can be invoked from any of the Peer Graphing API functions involving records, such as <a href="https://msdn.microsoft.com/9007095f-4f2a-4e92-895b-9a4033f0f7b9">PeerGraphUpdateRecord</a>. 




## -see-also




<a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a>



<a href="https://msdn.microsoft.com/d2451b45-eb42-4401-ab1d-505a41e25822">PEER_RECORD_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a>



<a href="https://msdn.microsoft.com/a9a48d8a-f31e-4526-bd09-826f04a564b1">PeerGraphValidateDeferredRecords</a>
 

 

