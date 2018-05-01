---
UID: NC:p2p.PFNPEER_SECURE_RECORD
title: PFNPEER_SECURE_RECORD
author: windows-driver-content
description: The PFNPEER_SECURE_RECORD callback specifies the function that the Peer Graphing Infrastructure calls to secure records.
old-location: p2p\pfnpeer_secure_record.htm
old-project: P2PSdk
ms.assetid: 454b40f6-a7de-4b59-ae35-a809c4510133
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PFNPEER_SECURE_RECORD, PFNPEER_SECURE_RECORD callback function [Peer Networking], p2p.pfnpeer_secure_record, p2p/PFNPEER_SECURE_RECORD
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: OPM_STANDARD_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	P2P.h
api_name:
-	PFNPEER_SECURE_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PFNPEER_SECURE_RECORD callback


## -description



      The <b>PFNPEER_SECURE_RECORD</b> callback specifies the function that the Peer Graphing Infrastructure calls     to secure records.


## -parameters




### -param hGraph [in]

Specifies the peer graph associated with the specified record.


### -param pvContext [in]

Pointer to the security context. This parameter  points to the <b>pvContext</b> member of the <a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a> structure.


### -param pRecord [in]

Pointer to the record to secure.


### -param changeType [in]

Specifies the reason the validation must occur.     <a href="https://msdn.microsoft.com/d2451b45-eb42-4401-ab1d-505a41e25822">PEER_RECORD_CHANGE_TYPE</a> enumerates the valid values.


### -param *ppSecurityData [out]

Specifies the security data for this record. This data is released by calling the method specified in the <b>pfnFreeSecurityData</b> member of the <a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a> after the data is copied and added to the record.


## -returns



If this callback succeeds, the return value is S_OK.




## -remarks



This callback is invoked whenever an application calls any of the methods that modify records, such as <a href="https://msdn.microsoft.com/8256e379-e5d5-4aef-ab05-e220602edf12">PeerGraphAddRecord</a> or <a href="https://msdn.microsoft.com/9007095f-4f2a-4e92-895b-9a4033f0f7b9">PeerGraphUpdateRecord</a>. This callback  
should create  data that is specific to this record, such as a small digital signature, and return it through the <i>ppSecurityData</i> parameter.
This data is then  added to the record in the <b>securityData</b> member, and is  verified by the method specified by the <b>pfnValidateRecord</b> member of the <a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a>.

<div class="alert"><b>Note</b>  This process happens on the local computer as well as any peer connected to the graph when the peer receives the record.</div>
<div> </div>
 If the operation specified by the <i>changeType</i> parameter is not allowed, the callback should return a failure code, such as PEER_E_NOT_AUTHORIZED,  instead of S_OK.

This callback can be invoked from any of the Peer Graphing API functions involving records, such as <a href="https://msdn.microsoft.com/9007095f-4f2a-4e92-895b-9a4033f0f7b9">PeerGraphUpdateRecord</a>. 




## -see-also




<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">
        PEER_DATA</a>



<a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">
        PEER_RECORD</a>



<a href="https://msdn.microsoft.com/d2451b45-eb42-4401-ab1d-505a41e25822">
        PEER_RECORD_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">
        PEER_SECURITY_INTERFACE</a>
 

 

