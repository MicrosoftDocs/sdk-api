---
UID: NC:p2p.PFNPEER_FREE_SECURITY_DATA
title: PFNPEER_FREE_SECURITY_DATA
author: windows-driver-content
description: The PFNPEER_FREE_SECURITY_DATA callback specifies the function that the Peer Graphing Infrastructure calls to free data returned by PFNPEER_SECURE_RECORD and PFNPEER_VALIDATE_RECORD callbacks.
old-location: p2p\pfnpeer_free_security_data.htm
old-project: P2PSdk
ms.assetid: aa340e32-6d7f-4218-b120-8c352fdbda0f
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PFNPEER_FREE_SECURITY_DATA, PFNPEER_FREE_SECURITY_DATA callback, PFNPEER_FREE_SECURITY_DATA callback function [Peer Networking], p2p.pfnpeer_free_security_data, p2p/PFNPEER_FREE_SECURITY_DATA
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
-	PFNPEER_FREE_SECURITY_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PFNPEER_FREE_SECURITY_DATA callback function


## -description



      The <b>PFNPEER_FREE_SECURITY_DATA</b> callback specifies the function that the Peer Graphing Infrastructure calls     to free data returned by <a href="https://msdn.microsoft.com/454b40f6-a7de-4b59-ae35-a809c4510133">PFNPEER_SECURE_RECORD</a> and <a href="https://msdn.microsoft.com/5d81f09b-e46b-43e6-b0a8-ed7c236f2968">PFNPEER_VALIDATE_RECORD</a>  callbacks.


## -parameters




### -param hGraph [in]

Specifies the peer graph associated with the specified record.


### -param pvContext [in]

Pointer to the security context to free. This  parameter is set to the value of the <b>pvContext</b> member of the <a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">PEER_SECURITY_INTERFACE</a> structure passed in <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a> or <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>.


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



This callback can be invoked from any of the Peer Graphing API functions involving records, such as <a href="https://msdn.microsoft.com/9007095f-4f2a-4e92-895b-9a4033f0f7b9">PeerGraphUpdateRecord</a>. 




## -see-also




<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">
        PEER_DATA</a>



<a href="https://msdn.microsoft.com/b4331cfc-dc1a-490b-b21d-0550f1d3fe33">
        PEER_SECURITY_INTERFACE</a>



<a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>



<a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>
 

 

