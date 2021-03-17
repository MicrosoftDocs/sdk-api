---
UID: NF:certenroll.IX509NameValuePairs.Remove
title: IX509NameValuePairs::Remove (certenroll.h)
description: Removes an IX509NameValuePair object from the collection by index number.
helpviewer_keywords: ["IX509NameValuePairs interface [Security]","Remove method","IX509NameValuePairs.Remove","IX509NameValuePairs::Remove","Remove","Remove method [Security]","Remove method [Security]","IX509NameValuePairs interface","certenroll/IX509NameValuePairs::Remove","security.ix509namevaluepairs_remove_method"]
old-location: security\ix509namevaluepairs_remove_method.htm
tech.root: security
ms.assetid: f66dbfd1-331f-4e1b-a17e-f8071044d073
ms.date: 12/05/2018
ms.keywords: IX509NameValuePairs interface [Security],Remove method, IX509NameValuePairs.Remove, IX509NameValuePairs::Remove, Remove, Remove method [Security], Remove method [Security],IX509NameValuePairs interface, certenroll/IX509NameValuePairs::Remove, security.ix509namevaluepairs_remove_method
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
 - IX509NameValuePairs::Remove
 - certenroll/IX509NameValuePairs::Remove
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
 - IX509NameValuePairs.Remove
---

# IX509NameValuePairs::Remove


## -description

The <b>Remove</b> method removes an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">IX509NameValuePair</a> object from the collection by index number.

## -parameters

### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">IX509NameValuePair</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepairs">IX509NameValuePairs</a>