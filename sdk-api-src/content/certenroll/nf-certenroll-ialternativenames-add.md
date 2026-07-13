---
UID: NF:certenroll.IAlternativeNames.Add
title: IAlternativeNames::Add (certenroll.h)
description: Adds an object to the collection. (IAlternativeNames.Add)
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","IAlternativeNames interface","IAlternativeNames interface [Security]","Add method","IAlternativeNames.Add","IAlternativeNames::Add","certenroll/IAlternativeNames::Add","security.ialternativenames_add_method"]
old-location: security\ialternativenames_add_method.htm
tech.root: security
ms.assetid: 02085a1c-0821-4b11-95ad-e1c3a69f4e80
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],IAlternativeNames interface, IAlternativeNames interface [Security],Add method, IAlternativeNames.Add, IAlternativeNames::Add, certenroll/IAlternativeNames::Add, security.ialternativenames_add_method
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
 - IAlternativeNames::Add
 - certenroll/IAlternativeNames::Add
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
 - IAlternativeNames.Add
---

# IAlternativeNames::Add


## -description

The <b>Add</b> method adds an object to the collection.

## -parameters

### -param pVal [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a> interface to add.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativenames">IAlternativeNames</a>
