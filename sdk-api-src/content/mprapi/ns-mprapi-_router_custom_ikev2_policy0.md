---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _ROUTER_CUSTOM_IKEv2_POLICY0 structure


## -description


Contains the IKEv2 main mode and quick mode policy configuration.

Do not use the  <b>ROUTER_CUSTOM_IKEv2_POLICY0</b> structure directly in your code; using <a href="https://msdn.microsoft.com/6CF919BD-E1E9-423F-8186-C992A5E6AB89">ROUTER_CUSTOM_IKEv2_POLICY</a> instead ensures that the proper version, based on the operating system the code in compiled under, is used.


## -struct-fields




### -field dwIntegrityMethod

A value that specifies the integrity algorithm to be negotiated during IKEv2 main mode SA negotiation. The allowed values for this member are defined in <a href="https://msdn.microsoft.com/f4a5b6b9-5cf1-48a4-811c-9150550688d8">IKEEXT_INTEGRITY_TYPE</a>.


### -field dwEncryptionMethod

A value that specifies the encryption algorithm to be negotiated during IKEv2 main mode SA negotiation. The allowed valued for this member are defined in <a href="https://msdn.microsoft.com/00d5def0-5c8c-4d84-b929-aec76a1a7110">IKEEXT_CIPHER_TYPE</a>.


### -field dwCipherTransformConstant

A value that specifies the encryption algorithm to be negotiated during IKEv2 quick mode SA negotiation. The allowed valued for this member are defined in <a href="https://msdn.microsoft.com/88bcd239-83a6-4bc6-b9c8-2416c91ee4c4">IPSEC_CIPHER_TYPE</a>.


### -field dwAuthTransformConstant

A value that specifies the hash algorithm to be negotiated during IKEv2 quick mode SA negotiation. The allowed valued for this member are defined in <a href="https://msdn.microsoft.com/9130ffa3-b757-42fa-b6bb-d380f2dbdbcb">IPSEC_AUTH_TYPE</a>.


### -field dwPfsGroup

A value that specifies the Diffie Hellman algorithm that should be used for Quick Mode PFS (Perfect Forward Secrecy). The allowed valued for this member are defined in <a href="https://msdn.microsoft.com/0f0ea028-859b-42ca-a4e3-fe23f0836883">IPSEC_PFS_GROUP</a>.


### -field dwDhGroup

A value that specifies the type of Diffie Hellman group used for Internet Key Exchange (IKE) key generation during MM SA negotiation. The allowed valued for this member are defined in <a href="https://msdn.microsoft.com/ed90c404-f713-4a0d-9698-eece1bfb7dd7">IKEEXT_DH_GROUP</a>.

