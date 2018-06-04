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

# ICertSrvSetupKeyInformation::put_ProviderName


## -description


The <b>ProviderName</b> property gets or sets the name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) or <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key storage provider</a> (KSP) that is used to generate or store the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.

This property is read/write.


## -parameters


## -remarks



For a KSP, the <b>ProviderName</b> property value must be formatted as <i>PublicKeyAlgorithmName</i>, number sign (#), and <i>KeyStorageProviderName</i>, for example "RSA#Microsoft Software Key Storage Provider" or "ECDSA_P256#Microsoft Software Key Storage Provider". The <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key algorithm</a> must be supported by the provider. To get supported algorithms, call the <a href="https://msdn.microsoft.com/ea4f270b-c556-4f52-892a-199c9cfced26">NCryptEnumAlgorithms</a> function with the <i>dwAlgOperations</i> parameter set to <b>NCRYPT_SIGNATURE_OPERATION</b>. For information about algorithm identifiers, see <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a>.




## -see-also




<a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a>
 

 

