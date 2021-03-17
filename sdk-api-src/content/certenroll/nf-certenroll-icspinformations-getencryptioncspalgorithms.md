---
UID: NF:certenroll.ICspInformations.GetEncryptionCspAlgorithms
title: ICspInformations::GetEncryptionCspAlgorithms (certenroll.h)
description: Retrieves the collection of encryption algorithms supported by a provider.
helpviewer_keywords: ["GetEncryptionCspAlgorithms","GetEncryptionCspAlgorithms method [Security]","GetEncryptionCspAlgorithms method [Security]","ICspInformations interface","ICspInformations interface [Security]","GetEncryptionCspAlgorithms method","ICspInformations.GetEncryptionCspAlgorithms","ICspInformations::GetEncryptionCspAlgorithms","certenroll/ICspInformations::GetEncryptionCspAlgorithms","security.icspinformations_getencryptioncspalgorithms_method"]
old-location: security\icspinformations_getencryptioncspalgorithms_method.htm
tech.root: security
ms.assetid: 85d2507c-0d0c-47a3-beb9-62af42b3ca3f
ms.date: 12/05/2018
ms.keywords: GetEncryptionCspAlgorithms, GetEncryptionCspAlgorithms method [Security], GetEncryptionCspAlgorithms method [Security],ICspInformations interface, ICspInformations interface [Security],GetEncryptionCspAlgorithms method, ICspInformations.GetEncryptionCspAlgorithms, ICspInformations::GetEncryptionCspAlgorithms, certenroll/ICspInformations::GetEncryptionCspAlgorithms, security.icspinformations_getencryptioncspalgorithms_method
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
 - ICspInformations::GetEncryptionCspAlgorithms
 - certenroll/ICspInformations::GetEncryptionCspAlgorithms
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
 - ICspInformations.GetEncryptionCspAlgorithms
---

# ICspInformations::GetEncryptionCspAlgorithms


## -description

The <b>GetEncryptionCspAlgorithms</b> method retrieves the collection of encryption algorithms supported by a provider.

## -parameters

### -param pCspInformation [in, optional]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> interface that represents the provider. This can be a legacy cryptographic service provider (CSP), a Cryptography API: Next Generation (CNG) provider, or <b>NULL</b>. If you specify <b>NULL</b>, this method returns the collection of all encryption algorithms supported by all CSPs and CNG providers.

### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithms">ICspAlgorithms</a> interface that represents the collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>