---
UID: NF:certenroll.IX509NameValuePair.Initialize
title: IX509NameValuePair::Initialize (certenroll.h)
description: Initializes the object from strings that contain the name and associated value.
helpviewer_keywords: ["IX509NameValuePair interface [Security]","Initialize method","IX509NameValuePair.Initialize","IX509NameValuePair::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509NameValuePair interface","certenroll/IX509NameValuePair::Initialize","security.ix509namevaluepair_initialize_method"]
old-location: security\ix509namevaluepair_initialize_method.htm
tech.root: security
ms.assetid: 3e935718-a59a-443e-bff2-a010a41e7756
ms.date: 12/05/2018
ms.keywords: IX509NameValuePair interface [Security],Initialize method, IX509NameValuePair.Initialize, IX509NameValuePair::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509NameValuePair interface, certenroll/IX509NameValuePair::Initialize, security.ix509namevaluepair_initialize_method
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
 - IX509NameValuePair::Initialize
 - certenroll/IX509NameValuePair::Initialize
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
 - IX509NameValuePair.Initialize
---

# IX509NameValuePair::Initialize


## -description

The <b>Initialize</b> method initializes the object from strings that contain the  name and associated value.

## -parameters

### -param strName [in]

A <b>BSTR</b> variable that contains the name.

### -param strValue [in]

A <b>BSTR</b> variable that contains the value.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509namevaluepair-get_name">Name</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509namevaluepair-get_value">Value</a> properties to retrieve the values initialized by calling this method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">IX509NameValuePair</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509namevaluepair-get_name">Name</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509namevaluepair-get_value">Value</a>