---
UID: NF:certenroll.IX509Extensions.AddRange
title: IX509Extensions::AddRange (certenroll.h)
description: Adds a range of IX509Extension objects to the collection.
old-location: security\ix509extensions_addrange_method.htm
tech.root: seccertenroll
ms.assetid: e2e11b36-966b-497a-a199-41364314d287
ms.date: 12/05/2018
ms.keywords: AddRange, AddRange method [Security], AddRange method [Security],IX509Extensions interface, IX509Extensions interface [Security],AddRange method, IX509Extensions.AddRange, IX509Extensions::AddRange, certenroll/IX509Extensions::AddRange, security.ix509extensions_addrange_method
ms.topic: method
f1_keywords:
- certenroll/IX509Extensions.AddRange
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- IX509Extensions.AddRange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509Extensions::AddRange


## -description


The <b>AddRange</b> method adds a range of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a> objects to the collection.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> interface that contains the collection to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a>
 

 

