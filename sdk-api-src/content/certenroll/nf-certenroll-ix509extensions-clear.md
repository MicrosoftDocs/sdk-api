---
UID: NF:certenroll.IX509Extensions.Clear
title: IX509Extensions::Clear (certenroll.h)
description: Removes all IX509Extension objects from the collection.
helpviewer_keywords: ["Clear","Clear method [Security]","Clear method [Security]","IX509Extensions interface","IX509Extensions interface [Security]","Clear method","IX509Extensions.Clear","IX509Extensions::Clear","certenroll/IX509Extensions::Clear","security.ix509extensions_clear_method"]
old-location: security\ix509extensions_clear_method.htm
tech.root: security
ms.assetid: a985521d-7fcc-49e6-b625-4038939da2ca
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Security], Clear method [Security],IX509Extensions interface, IX509Extensions interface [Security],Clear method, IX509Extensions.Clear, IX509Extensions::Clear, certenroll/IX509Extensions::Clear, security.ix509extensions_clear_method
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
 - IX509Extensions::Clear
 - certenroll/IX509Extensions::Clear
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
 - IX509Extensions.Clear
---

# IX509Extensions::Clear


## -description

The <b>Clear</b> method removes all <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a> objects from the collection.



## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a>
