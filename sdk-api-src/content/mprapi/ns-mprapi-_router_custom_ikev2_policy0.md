---
UID: NS:mprapi._ROUTER_CUSTOM_IKEv2_POLICY0
title: "_ROUTER_CUSTOM_IKEv2_POLICY0"
author: windows-driver-content
description: Contains the IKEv2 main mode and quick mode policy configuration.
old-location: rras\router_custom_ikev2_policy0.htm
old-project: RRAS
ms.assetid: 46ea7b05-0d2d-4ba1-b3c3-fab67eabf552
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PROUTER_CUSTOM_IKEv2_POLICY0, *PROUTER_CUSTOM_L2TP_POLICY0, PROUTER_CUSTOM_IKEv2_POLICY0, PROUTER_CUSTOM_IKEv2_POLICY0 structure pointer [RAS], ROUTER_CUSTOM_IKEv2_POLICY0, ROUTER_CUSTOM_IKEv2_POLICY0 structure [RAS], ROUTER_CUSTOM_L2TP_POLICY0, _ROUTER_CUSTOM_IKEv2_POLICY0, mprapi/PROUTER_CUSTOM_IKEv2_POLICY0, mprapi/ROUTER_CUSTOM_IKEv2_POLICY0, rras.router_custom_ikev2_policy0"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROUTER_CUSTOM_IKEv2_POLICY0, *PROUTER_CUSTOM_IKEv2_POLICY0, ROUTER_CUSTOM_L2TP_POLICY0, *PROUTER_CUSTOM_L2TP_POLICY0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mprapi.h
api_name:
-	ROUTER_CUSTOM_IKEv2_POLICY0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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

