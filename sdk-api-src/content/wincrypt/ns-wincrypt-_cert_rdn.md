---
UID: NS:wincrypt._CERT_RDN
title: "_CERT_RDN"
author: windows-driver-content
description: The CERT_RDN structure contains a relative distinguished name (RDN) consisting of an array of CERT_RDN_ATTR structures.
old-location: security\cert_rdn.htm
old-project: SecCrypto
ms.assetid: e84254b9-e9a7-4689-a12f-2772282c5433
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: "*PCERT_RDN, CERT_RDN, CERT_RDN structure [Security], PCERT_RDN, PCERT_RDN structure pointer [Security], _CERT_RDN, _crypto2_cert_rdn, security.cert_rdn, wincrypt/CERT_RDN, wincrypt/PCERT_RDN"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CERT_RDN, *PCERT_RDN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CERT_RDN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_RDN structure


## -description


The <b>CERT_RDN</b> structure contains a <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">relative distinguished name</a> (RDN) consisting of an array of 
<a href="https://msdn.microsoft.com/4729e824-761c-4115-8b7b-76ffdab8ea62">CERT_RDN_ATTR</a> structures.


## -struct-fields




### -field cRDNAttr

Number of elements in the <b>rgRDNAttr</b> array.


### -field rgRDNAttr

Array of 
<a href="https://msdn.microsoft.com/4729e824-761c-4115-8b7b-76ffdab8ea62">CERT_RDN_ATTR</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/402d1051-d91a-4a79-96f6-10ed96a32d5c">CERT_NAME_INFO</a>



<a href="https://msdn.microsoft.com/4729e824-761c-4115-8b7b-76ffdab8ea62">CERT_RDN_ATTR</a>



<a href="https://msdn.microsoft.com/20b3fcfb-55df-46ff-80a5-70f31a3d03b2">CertFindCertificateInStore</a>



<a href="https://msdn.microsoft.com/e45b80a3-9269-4f21-8407-1c8303cb5f32">CertIsRDNAttrsInCertificateName</a>



<a href="https://msdn.microsoft.com/b3d96de8-5cbc-4ccb-b759-6757520bbda3">CertNameToStr</a>
 

 

