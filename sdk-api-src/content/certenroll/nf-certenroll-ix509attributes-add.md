---
UID: NF:certenroll.IX509Attributes.Add
title: IX509Attributes::Add (certenroll.h)
description: Adds an IX509Attribute object to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","IX509Attributes interface","IX509Attributes interface [Security]","Add method","IX509Attributes.Add","IX509Attributes::Add","certenroll/IX509Attributes::Add","security.ix509attributes_add_method"]
old-location: security\ix509attributes_add_method.htm
tech.root: security
ms.assetid: 769293d8-0ae0-419f-9399-3c501d700251
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],IX509Attributes interface, IX509Attributes interface [Security],Add method, IX509Attributes.Add, IX509Attributes::Add, certenroll/IX509Attributes::Add, security.ix509attributes_add_method
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
 - IX509Attributes::Add
 - certenroll/IX509Attributes::Add
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
 - IX509Attributes.Add
---

# IX509Attributes::Add


## -description

The <b>Add</b> method adds an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a> object to the collection.

## -parameters

### -param pVal [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a> interface that represents the attribute to add to the collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>