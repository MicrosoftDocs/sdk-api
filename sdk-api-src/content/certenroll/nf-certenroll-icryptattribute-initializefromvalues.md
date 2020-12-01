---
UID: NF:certenroll.ICryptAttribute.InitializeFromValues
title: ICryptAttribute::InitializeFromValues (certenroll.h)
description: Initializes a cryptographic attribute by using an IX509Attributes object.
helpviewer_keywords: ["ICryptAttribute interface [Security]","InitializeFromValues method","ICryptAttribute.InitializeFromValues","ICryptAttribute::InitializeFromValues","InitializeFromValues","InitializeFromValues method [Security]","InitializeFromValues method [Security]","ICryptAttribute interface","certenroll/ICryptAttribute::InitializeFromValues","security.icryptattribute_initializefromvalues_method"]
old-location: security\icryptattribute_initializefromvalues_method.htm
tech.root: security
ms.assetid: 763fd244-173d-4b0b-8809-e98c18b8e5b5
ms.date: 12/05/2018
ms.keywords: ICryptAttribute interface [Security],InitializeFromValues method, ICryptAttribute.InitializeFromValues, ICryptAttribute::InitializeFromValues, InitializeFromValues, InitializeFromValues method [Security], InitializeFromValues method [Security],ICryptAttribute interface, certenroll/ICryptAttribute::InitializeFromValues, security.icryptattribute_initializefromvalues_method
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
 - ICryptAttribute::InitializeFromValues
 - certenroll/ICryptAttribute::InitializeFromValues
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
 - ICryptAttribute.InitializeFromValues
---

# ICryptAttribute::InitializeFromValues


## -description

The <b>InitializeFromValues</b> method initializes a cryptographic attribute by using an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a> object.

## -parameters

### -param pAttributes [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a> interface that contains the attribute collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>InitializeFromValues</b> method uses the first <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a> object in the collection.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>