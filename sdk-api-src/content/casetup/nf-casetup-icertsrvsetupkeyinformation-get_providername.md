---
UID: NF:casetup.ICertSrvSetupKeyInformation.get_ProviderName
title: ICertSrvSetupKeyInformation::get_ProviderName
author: windows-sdk-content
description: Gets or sets the name of the cryptographic service provider (CSP) or key storage provider (KSP) that is used to generate or store the private key.
old-location: security\icertsrvsetupkeyinformation_providername.htm
tech.root: SecCrypto
ms.assetid: a8f50b34-0403-40c0-9ecb-f663ccbd622a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICertSrvSetupKeyInformation interface [Security],ProviderName property, ICertSrvSetupKeyInformation.ProviderName, ICertSrvSetupKeyInformation.get_ProviderName, ICertSrvSetupKeyInformation::ProviderName, ICertSrvSetupKeyInformation::get_ProviderName, ICertSrvSetupKeyInformation::put_ProviderName, ProviderName property [Security], ProviderName property [Security],ICertSrvSetupKeyInformation interface, casetup/ICertSrvSetupKeyInformation::ProviderName, casetup/ICertSrvSetupKeyInformation::get_ProviderName, casetup/ICertSrvSetupKeyInformation::put_ProviderName, get_ProviderName, security.icertsrvsetupkeyinformation_providername
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
 - ICertSrvSetupKeyInformation.ProviderName
 - ICertSrvSetupKeyInformation.get_ProviderName
 - ICertSrvSetupKeyInformation.put_ProviderName
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
- ICertSrvSetupKeyInformation.get_ProviderName
: 
---

# ICertSrvSetupKeyInformation::get_ProviderName


## -description


The <b>ProviderName</b> property gets or sets the name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) or <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key storage provider</a> (KSP) that is used to generate or store the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.

This property is read/write.


## -parameters


## -remarks



For a KSP, the <b>ProviderName</b> property value must be formatted as <i>PublicKeyAlgorithmName</i>, number sign (#), and <i>KeyStorageProviderName</i>, for example "RSA#Microsoft Software Key Storage Provider" or "ECDSA_P256#Microsoft Software Key Storage Provider". The <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key algorithm</a> must be supported by the provider. To get supported algorithms, call the <a href="https://msdn.microsoft.com/ea4f270b-c556-4f52-892a-199c9cfced26">NCryptEnumAlgorithms</a> function with the <i>dwAlgOperations</i> parameter set to <b>NCRYPT_SIGNATURE_OPERATION</b>. For information about algorithm identifiers, see <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a>.




## -see-also




<a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a>
 

 

