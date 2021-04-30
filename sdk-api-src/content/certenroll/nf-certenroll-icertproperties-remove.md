---
UID: NF:certenroll.ICertProperties.Remove
title: ICertProperties::Remove (certenroll.h)
description: Removes a property from the collection by index value.
helpviewer_keywords: ["ICertProperties interface [Security]","Remove method","ICertProperties.Remove","ICertProperties::Remove","Remove","Remove method [Security]","Remove method [Security]","ICertProperties interface","certenroll/ICertProperties::Remove","security.icertproperties_remove_method"]
old-location: security\icertproperties_remove_method.htm
tech.root: security
ms.assetid: 7ee9e624-6f27-4177-9711-7062cb10f77b
ms.date: 12/05/2018
ms.keywords: ICertProperties interface [Security],Remove method, ICertProperties.Remove, ICertProperties::Remove, Remove, Remove method [Security], Remove method [Security],ICertProperties interface, certenroll/ICertProperties::Remove, security.icertproperties_remove_method
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
 - ICertProperties::Remove
 - certenroll/ICertProperties::Remove
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
 - ICertProperties.Remove
---

# ICertProperties::Remove


## -description

The <b>Remove</b> method removes a property from the collection by index value.

## -parameters

### -param Index [in]

A <b>LONG</b> variable that contains the index of the property to remove.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>