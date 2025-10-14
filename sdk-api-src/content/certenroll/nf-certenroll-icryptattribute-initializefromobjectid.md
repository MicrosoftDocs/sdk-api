---
UID: NF:certenroll.ICryptAttribute.InitializeFromObjectId
title: ICryptAttribute::InitializeFromObjectId (certenroll.h)
description: Initializes a cryptographic attribute by using an object identifier.
helpviewer_keywords: ["ICryptAttribute interface [Security]","InitializeFromObjectId method","ICryptAttribute.InitializeFromObjectId","ICryptAttribute::InitializeFromObjectId","InitializeFromObjectId","InitializeFromObjectId method [Security]","InitializeFromObjectId method [Security]","ICryptAttribute interface","certenroll/ICryptAttribute::InitializeFromObjectId","security.icryptattribute_initializefromobjectid_method"]
old-location: security\icryptattribute_initializefromobjectid_method.htm
tech.root: security
ms.assetid: 6825cca7-c3a5-46a8-9be5-851344629929
ms.date: 12/05/2018
ms.keywords: ICryptAttribute interface [Security],InitializeFromObjectId method, ICryptAttribute.InitializeFromObjectId, ICryptAttribute::InitializeFromObjectId, InitializeFromObjectId, InitializeFromObjectId method [Security], InitializeFromObjectId method [Security],ICryptAttribute interface, certenroll/ICryptAttribute::InitializeFromObjectId, security.icryptattribute_initializefromobjectid_method
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
 - ICryptAttribute::InitializeFromObjectId
 - certenroll/ICryptAttribute::InitializeFromObjectId
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
 - ICryptAttribute.InitializeFromObjectId
---

# ICryptAttribute::InitializeFromObjectId


## -description

The <b>InitializeFromObjectId</b> method initializes a cryptographic attribute by using an object identifier.

## -parameters

### -param pObjectId [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that contains the object identifier of the attribute.

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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The pointer to the <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromname">InitializeFromName</a> or <a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromvalue">InitializeFromValue</a> methods before using it in this method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>