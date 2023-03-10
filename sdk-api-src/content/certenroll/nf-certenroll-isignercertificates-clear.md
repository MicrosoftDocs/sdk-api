---
UID: NF:certenroll.ISignerCertificates.Clear
title: ISignerCertificates::Clear (certenroll.h)
description: Removes all ISignerCertificate objects from the collection.
helpviewer_keywords: ["Clear","Clear method [Security]","Clear method [Security]","ISignerCertificates interface","ISignerCertificates interface [Security]","Clear method","ISignerCertificates.Clear","ISignerCertificates::Clear","certenroll/ISignerCertificates::Clear","security.isignercertificates_clear_method"]
old-location: security\isignercertificates_clear_method.htm
tech.root: security
ms.assetid: 8be3f0d4-db41-408d-bd4b-37c41b1b1c54
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Security], Clear method [Security],ISignerCertificates interface, ISignerCertificates interface [Security],Clear method, ISignerCertificates.Clear, ISignerCertificates::Clear, certenroll/ISignerCertificates::Clear, security.isignercertificates_clear_method
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
 - ISignerCertificates::Clear
 - certenroll/ISignerCertificates::Clear
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
 - ISignerCertificates.Clear
---

# ISignerCertificates::Clear


## -description

The <b>Clear</b> method removes all <a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> objects from the collection.



## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificates">ISignerCertificates</a>
