---
UID: NF:certenroll.IX509NameValuePairs.Add
title: IX509NameValuePairs::Add (certenroll.h)
description: Adds an IX509NameValuePair object to the collection.helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","IX509NameValuePairs interface","IX509NameValuePairs interface [Security]","Add method","IX509NameValuePairs.Add","IX509NameValuePairs::Add","certenroll/IX509NameValuePairs::Add","security.ix509namevaluepairs_add_method"]
old-location: security\ix509namevaluepairs_add_method.htm
tech.root: seccertenroll
ms.assetid: 2b5592d4-4f3b-4cea-8c59-15529cc53efa
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],IX509NameValuePairs interface, IX509NameValuePairs interface [Security],Add method, IX509NameValuePairs.Add, IX509NameValuePairs::Add, certenroll/IX509NameValuePairs::Add, security.ix509namevaluepairs_add_method
f1_keywords:
- certenroll/IX509NameValuePairs.Add
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
- IX509NameValuePairs.Add
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509NameValuePairs::Add


## -description


The <b>Add</b> method adds an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">IX509NameValuePair</a> object to the collection.


## -parameters




### -param pVal [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">IX509NameValuePair</a> interface that represents the name-value pair to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">IX509NameValuePair</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepairs">IX509NameValuePairs</a>
 

 

