---
UID: NN:certenroll.ICspAlgorithm
title: ICspAlgorithm (certenroll.h)
description: Represents an algorithm implemented by a cryptographic provider.
helpviewer_keywords: ["ICspAlgorithm","ICspAlgorithm interface [Security]","ICspAlgorithm interface [Security]","described","certenroll/ICspAlgorithm","security.icspalgorithm"]
old-location: security\icspalgorithm.htm
tech.root: security
ms.assetid: 08eba616-2e96-40cd-9fda-8549de98c138
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm, ICspAlgorithm interface [Security], ICspAlgorithm interface [Security],described, certenroll/ICspAlgorithm, security.icspalgorithm
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspAlgorithm
 - certenroll/ICspAlgorithm
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspAlgorithm
---

# ICspAlgorithm interface


## -description

The <b>ICspAlgorithm</b> interface represents an algorithm implemented by a cryptographic provider. Providers are separate modules that implement encryption, hashing, signing, and key exchange (archival)  algorithms. Similar providers are grouped together in a type. For example, the <a href="/windows/desktop/SecCrypto/prov-rsa-full">PROV_RSA_FULL</a> type identifies providers that typically support the following algorithms. An individual provider can, however,  choose to support fewer or more algorithms than those listed.<ul>
<li>Encryption: RC2, RC4</li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: RSA</li>
<li>Signature: RSA</li>
</ul>For more information, see <a href="/windows/desktop/SecCrypto/microsoft-cryptographic-service-providers">Microsoft Cryptographic Service Providers</a>. 

A collection of <b>ICspAlgorithm</b> objects can be retrieved from an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object. The <b>ICspInformation</b> object can be initialized from a provider name or type.

## -inheritance

The <b>ICspAlgorithm</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICspAlgorithm</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/SecCrypto/cryptographic-service-providers">Cryptographic Service Providers</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
