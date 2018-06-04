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

# ICertSrvSetupKeyInformation::get_HashAlgorithm


## -description


The <b>HashAlgorithm</b> property gets or sets the name of the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing algorithm</a> used to  sign or verify the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) certificate for the key.

This property is read/write.


## -parameters


## -remarks



The hashing algorithm must be supported by the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915743">ProviderName</a> provider. For <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> (CSPs), get supported algorithms by calling the <a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a> function for the given provider. For <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key storage providers</a> (KSPs), get supported algorithms by calling the <a href="https://msdn.microsoft.com/7fa227c0-2b80-49ab-8a19-72f8444d5507">BCryptEnumAlgorithms</a> function with the <i>dwAlgOperations</i> parameter set to <b>BCRYPT_HASH_OPERATION</b>. For information about algorithm identifiers, see <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a>.


#### Examples

For an example of enumerating supported algorithms by using <a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a>, see <a href="https://msdn.microsoft.com/10a5210d-7992-4832-9435-67ac2b851a97">Example C Program: Enumerating CSP Providers and Provider Types</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a>
 

 

