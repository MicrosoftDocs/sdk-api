---
UID: NF:certenroll.ICryptAttributes.AddRange
title: ICryptAttributes::AddRange (certenroll.h)
description: Adds a range of ICryptAttribute objects to the collection. The attributes are contained in another ICryptAttributes collection.
helpviewer_keywords: ["AddRange","AddRange method [Security]","AddRange method [Security]","ICryptAttributes interface","ICryptAttributes interface [Security]","AddRange method","ICryptAttributes.AddRange","ICryptAttributes::AddRange","certenroll/ICryptAttributes::AddRange","security.icryptattributes_addrange_method"]
old-location: security\icryptattributes_addrange_method.htm
tech.root: security
ms.assetid: 8dc0a2c5-3734-47c7-a716-f53322fee39d
ms.date: 12/05/2018
ms.keywords: AddRange, AddRange method [Security], AddRange method [Security],ICryptAttributes interface, ICryptAttributes interface [Security],AddRange method, ICryptAttributes.AddRange, ICryptAttributes::AddRange, certenroll/ICryptAttributes::AddRange, security.icryptattributes_addrange_method
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
 - ICryptAttributes::AddRange
 - certenroll/ICryptAttributes::AddRange
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
 - ICryptAttributes.AddRange
---

# ICryptAttributes::AddRange


## -description

The <b>AddRange</b> method adds a range of <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a> objects to the collection. The attributes are contained in another <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection.

## -parameters

### -param pValue [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> interface that contains the attribute collection to add.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>