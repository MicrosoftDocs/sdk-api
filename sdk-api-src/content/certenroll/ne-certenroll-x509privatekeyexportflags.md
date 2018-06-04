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

# X509PrivateKeyExportFlags enumeration


## -description


The <b>X509PrivateKeyExportFlags</b> enumeration type specifies the export policy for a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. For a Cryptography API: Next Generation (CNG) key, the policy is stored by the key service provider (KSP), and it is the responsibility of the KSP to enforce the policy. When a  legacy <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) is specified, the policy is used when creating the key, and it is the responsibility of the CSP to enforce the policy. This enumeration is used when specifying and retrieving the  <a href="https://msdn.microsoft.com/e3f04252-fe49-48fb-9e77-8a05031abf5f">ExportPolicy</a> property on the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> interface.


## -enum-fields




### -field XCN_NCRYPT_ALLOW_EXPORT_NONE

Export is not allowed. This is the default value.


### -field XCN_NCRYPT_ALLOW_EXPORT_FLAG

The private key can be exported.


### -field XCN_NCRYPT_ALLOW_PLAINTEXT_EXPORT_FLAG

The private key can be exported in plaintext form.


### -field XCN_NCRYPT_ALLOW_ARCHIVING_FLAG

The private key can be exported once for archiving.


### -field XCN_NCRYPT_ALLOW_PLAINTEXT_ARCHIVING_FLAG

The private key can be exported once in plaintext form for archiving.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

