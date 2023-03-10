---
UID: NF:certenroll.ISmimeCapabilities.Add
title: ISmimeCapabilities::Add (certenroll.h)
description: Adds an ISmimeCapability object to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","ISmimeCapabilities interface","ISmimeCapabilities interface [Security]","Add method","ISmimeCapabilities.Add","ISmimeCapabilities::Add","certenroll/ISmimeCapabilities::Add","security.ismimecapabilities_add_method"]
old-location: security\ismimecapabilities_add_method.htm
tech.root: security
ms.assetid: 8ad35758-0dc1-4887-aea7-b8ead537cab2
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],ISmimeCapabilities interface, ISmimeCapabilities interface [Security],Add method, ISmimeCapabilities.Add, ISmimeCapabilities::Add, certenroll/ISmimeCapabilities::Add, security.ismimecapabilities_add_method
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
 - ISmimeCapabilities::Add
 - certenroll/ISmimeCapabilities::Add
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
 - ISmimeCapabilities.Add
---

# ISmimeCapabilities::Add


## -description

The <b>Add</b> method adds an <a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a> object to the collection.

## -parameters

### -param pVal [in]

Pointer to the <a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a> interface to add.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapabilities">ISmimeCapabilities</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a>