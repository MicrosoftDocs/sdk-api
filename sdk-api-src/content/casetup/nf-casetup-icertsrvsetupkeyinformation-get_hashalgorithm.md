---
UID: NF:casetup.ICertSrvSetupKeyInformation.get_HashAlgorithm
title: ICertSrvSetupKeyInformation::get_HashAlgorithm
author: windows-sdk-content
description: Gets or sets the name of the hashing algorithm used to sign or verify the certification authority (CA) certificate for the key.
old-location: security\icertsrvsetupkeyinformation_hashalgorithm.htm
tech.root: seccrypto
ms.assetid: f1e007d1-eadb-4ab6-91bc-3c8a61b54aca
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: HashAlgorithm property [Security], HashAlgorithm property [Security],ICertSrvSetupKeyInformation interface, ICertSrvSetupKeyInformation interface [Security],HashAlgorithm property, ICertSrvSetupKeyInformation.HashAlgorithm, ICertSrvSetupKeyInformation.get_HashAlgorithm, ICertSrvSetupKeyInformation::HashAlgorithm, ICertSrvSetupKeyInformation::get_HashAlgorithm, ICertSrvSetupKeyInformation::put_HashAlgorithm, casetup/ICertSrvSetupKeyInformation::HashAlgorithm, casetup/ICertSrvSetupKeyInformation::get_HashAlgorithm, casetup/ICertSrvSetupKeyInformation::put_HashAlgorithm, get_HashAlgorithm, security.icertsrvsetupkeyinformation_hashalgorithm
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetupKeyInformation.HashAlgorithm
 - ICertSrvSetupKeyInformation.get_HashAlgorithm
 - ICertSrvSetupKeyInformation.put_HashAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- casetup.h
: 
- ICertSrvSetupKeyInformation.get_HashAlgorithm
: 
---

# ICertSrvSetupKeyInformation::get_HashAlgorithm


## -description


The <b>HashAlgorithm</b> property gets or sets the name of the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing algorithm</a> used to  sign or verify the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) certificate for the key.

This property is read/write.


## -parameters


## -remarks



The hashing algorithm must be supported by the <a href="https://msdn.microsoft.com/a8f50b34-0403-40c0-9ecb-f663ccbd622a">ProviderName</a> provider. For <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> (CSPs), get supported algorithms by calling the <a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a> function for the given provider. For <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key storage providers</a> (KSPs), get supported algorithms by calling the <a href="https://msdn.microsoft.com/7fa227c0-2b80-49ab-8a19-72f8444d5507">BCryptEnumAlgorithms</a> function with the <i>dwAlgOperations</i> parameter set to <b>BCRYPT_HASH_OPERATION</b>. For information about algorithm identifiers, see <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a>.


#### Examples

For an example of enumerating supported algorithms by using <a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a>, see <a href="https://msdn.microsoft.com/10a5210d-7992-4832-9435-67ac2b851a97">Example C Program: Enumerating CSP Providers and Provider Types</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a>
 

 

