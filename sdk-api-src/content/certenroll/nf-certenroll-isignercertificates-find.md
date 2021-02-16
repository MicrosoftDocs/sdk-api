---
UID: NF:certenroll.ISignerCertificates.Find
title: ISignerCertificates::Find (certenroll.h)
description: Retrieves the index number of an ISignerCertificate object.
helpviewer_keywords: ["Find","Find method [Security]","Find method [Security]","ISignerCertificates interface","ISignerCertificates interface [Security]","Find method","ISignerCertificates.Find","ISignerCertificates::Find","certenroll/ISignerCertificates::Find","security.isignercertificates_find_method"]
old-location: security\isignercertificates_find_method.htm
tech.root: security
ms.assetid: ee741eda-e125-4938-bc49-d8089f7d5df2
ms.date: 12/05/2018
ms.keywords: Find, Find method [Security], Find method [Security],ISignerCertificates interface, ISignerCertificates interface [Security],Find method, ISignerCertificates.Find, ISignerCertificates::Find, certenroll/ISignerCertificates::Find, security.isignercertificates_find_method
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
 - ISignerCertificates::Find
 - certenroll/ISignerCertificates::Find
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
 - ISignerCertificates.Find
---

# ISignerCertificates::Find


## -description

The <b>Find</b> method retrieves the index number of an <a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object.

## -parameters

### -param pSignerCert [in]

Pointer to the <a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> interface.

### -param piSignerCert [out]

Pointer to a <b>LONG</b> variable that receives the index number.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificates">ISignerCertificates</a>