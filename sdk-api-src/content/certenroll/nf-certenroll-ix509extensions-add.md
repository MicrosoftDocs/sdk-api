---
UID: NF:certenroll.IX509Extensions.Add
title: IX509Extensions::Add (certenroll.h)
description: Adds an IX509Extension object to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","IX509Extensions interface","IX509Extensions interface [Security]","Add method","IX509Extensions.Add","IX509Extensions::Add","certenroll/IX509Extensions::Add","security.ix509extensions_add_method"]
old-location: security\ix509extensions_add_method.htm
tech.root: security
ms.assetid: 08109828-44d9-4b8f-a57c-bbedfc82fbbb
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],IX509Extensions interface, IX509Extensions interface [Security],Add method, IX509Extensions.Add, IX509Extensions::Add, certenroll/IX509Extensions::Add, security.ix509extensions_add_method
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
 - IX509Extensions::Add
 - certenroll/IX509Extensions::Add
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
 - IX509Extensions.Add
---

# IX509Extensions::Add


## -description

The <b>Add</b> method adds an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a> object to the collection. This method is web enabled.

## -parameters

### -param pVal [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a> object to add to the collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a>