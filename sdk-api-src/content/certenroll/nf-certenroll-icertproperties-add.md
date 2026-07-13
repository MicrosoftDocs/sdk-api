---
UID: NF:certenroll.ICertProperties.Add
title: ICertProperties::Add (certenroll.h)
description: Adds a property to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","ICertProperties interface","ICertProperties interface [Security]","Add method","ICertProperties.Add","ICertProperties::Add","certenroll/ICertProperties::Add","security.icertproperties_add_method"]
old-location: security\icertproperties_add_method.htm
tech.root: security
ms.assetid: 53ea895d-0c41-445e-bfcc-2b2e53e10ff8
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICertProperties interface, ICertProperties interface [Security],Add method, ICertProperties.Add, ICertProperties::Add, certenroll/ICertProperties::Add, security.icertproperties_add_method
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
 - ICertProperties::Add
 - certenroll/ICertProperties::Add
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
 - ICertProperties.Add
---

# ICertProperties::Add


## -description

The <b>Add</b> method adds a property to the collection. This method is web enabled.

## -parameters

### -param pVal [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a> interface that represents the property to add to the collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
An item in the collection has the same ID as the property you specified.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>