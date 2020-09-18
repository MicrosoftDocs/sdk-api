---
UID: NF:certenroll.ICspInformations.GetHashAlgorithms
title: ICspInformations::GetHashAlgorithms (certenroll.h)
description: Retrieves the collection of hash algorithms supported by a provider.
helpviewer_keywords: ["GetHashAlgorithms","GetHashAlgorithms method [Security]","GetHashAlgorithms method [Security]","ICspInformations interface","ICspInformations interface [Security]","GetHashAlgorithms method","ICspInformations.GetHashAlgorithms","ICspInformations::GetHashAlgorithms","certenroll/ICspInformations::GetHashAlgorithms","security.icspinformations_gethashalgorithms_method"]
old-location: security\icspinformations_gethashalgorithms_method.htm
tech.root: security
ms.assetid: 647cad18-ed2e-4f3a-92d4-28fcfe60a800
ms.date: 12/05/2018
ms.keywords: GetHashAlgorithms, GetHashAlgorithms method [Security], GetHashAlgorithms method [Security],ICspInformations interface, ICspInformations interface [Security],GetHashAlgorithms method, ICspInformations.GetHashAlgorithms, ICspInformations::GetHashAlgorithms, certenroll/ICspInformations::GetHashAlgorithms, security.icspinformations_gethashalgorithms_method
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
 - ICspInformations::GetHashAlgorithms
 - certenroll/ICspInformations::GetHashAlgorithms
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
 - ICspInformations.GetHashAlgorithms
---

# ICspInformations::GetHashAlgorithms


## -description

The <b>GetHashAlgorithms</b> method retrieves the collection of hash algorithms supported by a provider.

## -parameters

### -param pCspInformation [in, optional]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> interface that represents the provider. This can be a legacy cryptographic service provider (CSP), a Cryptography API: Next Generation (CNG) provider, or <b>NULL</b>. If you specify <b>NULL</b>, this method returns the collection of all hash algorithms supported by all CSPs and CNG providers.

### -param ppValue [out]

Address of a pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> interface that represents the collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>