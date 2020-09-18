---
UID: NF:certenroll.ICryptAttributes.Add
title: ICryptAttributes::Add (certenroll.h)
description: Adds an ICryptAttribute object to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","ICryptAttributes interface","ICryptAttributes interface [Security]","Add method","ICryptAttributes.Add","ICryptAttributes::Add","certenroll/ICryptAttributes::Add","security.icryptattributes_add_method"]
old-location: security\icryptattributes_add_method.htm
tech.root: security
ms.assetid: a9288c74-3d7f-4293-b666-45c90a859166
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICryptAttributes interface, ICryptAttributes interface [Security],Add method, ICryptAttributes.Add, ICryptAttributes::Add, certenroll/ICryptAttributes::Add, security.icryptattributes_add_method
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
 - ICryptAttributes::Add
 - certenroll/ICryptAttributes::Add
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
 - ICryptAttributes.Add
---

# ICryptAttributes::Add


## -description

The <b>Add</b> method adds an <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a> object to the collection.

## -parameters

### -param pVal [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a> interface that represents the attribute to add.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>