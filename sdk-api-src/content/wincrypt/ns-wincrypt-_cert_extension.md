---
UID: NS:wincrypt._CERT_EXTENSION
title: "_CERT_EXTENSION"
author: windows-sdk-content
description: The CERT_EXTENSION structure contains the extension information for a certificate, Certificate Revocation List (CRL) or Certificate Trust List (CTL).
old-location: security\cert_extension.htm
tech.root: seccrypto
ms.assetid: 787a4df0-c0e3-46b9-a7e6-eb3bee3ed717
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCERT_EXTENSION, CERT_EXTENSION, CERT_EXTENSION structure [Security], PCERT_EXTENSION, PCERT_EXTENSION structure pointer [Security], _CERT_EXTENSION, _crypto2_cert_extension, security.cert_extension, wincrypt/CERT_EXTENSION, wincrypt/PCERT_EXTENSION"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_EXTENSION
product: Windows
targetos: Windows
req.typenames: CERT_EXTENSION, *PCERT_EXTENSION
req.redist: 
---

# _CERT_EXTENSION structure


## -description


The <b>CERT_EXTENSION</b> structure contains the extension information for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Revocation List</a> (CRL) or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Trust List</a> (CTL).


## -struct-fields




### -field pszObjId

<a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">Object identifier</a> (OID) that specifies the structure of the extension data contained in the <b>Value</b> member. For specifics on extension OIDs and their related structures, see 
<a href="cryptography_structures.htm">X.509 Certificate Extension Structures</a>.


### -field fCritical

If <b>TRUE</b>, any limitations specified by the extension in the <b>Value</b> member of this structure are imperative. If <b>FALSE</b>, limitations set by this extension can be ignored.


### -field Value

A 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_OBJID_BLOB</a> structure that contains the encoded extension data. The <b>cbData</b> member of <b>Value</b> indicates the length in bytes of the <b>pbData</b> member. The <b>pbData</b> member byte string is the encoded extension.


## -see-also




<a href="https://msdn.microsoft.com/b393ef08-cedb-4840-a427-10ead315d6ea">CERT_EXTENSIONS</a>



<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/30e7952a-a408-404f-9058-8197539387f6">CRL_ENTRY</a>



<a href="https://msdn.microsoft.com/06a28de3-dd7c-4efe-9baa-20aac69d63f3">CRL_INFO</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/ebc63847-b641-4205-b15c-7b32c1426c21">CTL_ENTRY</a>



<a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a>



<a href="https://msdn.microsoft.com/489c58b6-a704-4f54-bc64-34eacafc347c">CertFindExtension</a>
 

 

