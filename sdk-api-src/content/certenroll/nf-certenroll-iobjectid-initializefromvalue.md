---
UID: NF:certenroll.IObjectId.InitializeFromValue
title: IObjectId::InitializeFromValue (certenroll.h)
description: Initializes the object from a string that contains a dotted decimal object identifier (OID).
helpviewer_keywords: ["IObjectId interface [Security]","InitializeFromValue method","IObjectId.InitializeFromValue","IObjectId::InitializeFromValue","InitializeFromValue","InitializeFromValue method [Security]","InitializeFromValue method [Security]","IObjectId interface","certenroll/IObjectId::InitializeFromValue","security.iobjectid_initializefromvalue_method"]
old-location: security\iobjectid_initializefromvalue_method.htm
tech.root: security
ms.assetid: 2bb2ee69-02c3-41b9-a67b-036c7154a44e
ms.date: 12/05/2018
ms.keywords: IObjectId interface [Security],InitializeFromValue method, IObjectId.InitializeFromValue, IObjectId::InitializeFromValue, InitializeFromValue, InitializeFromValue method [Security], InitializeFromValue method [Security],IObjectId interface, certenroll/IObjectId::InitializeFromValue, security.iobjectid_initializefromvalue_method
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
 - IObjectId::InitializeFromValue
 - certenroll/IObjectId::InitializeFromValue
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
 - IObjectId.InitializeFromValue
---

# IObjectId::InitializeFromValue


## -description

The <b>InitializeFromValue</b> method initializes the object from a string that contains a dotted decimal <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). This method is web enabled.

## -parameters

### -param strValue [in]

A <b>BSTR</b> variable that contains the dotted decimal representation of the ASN.1 object identifier. For example, the value 1.2.840.10045.4.1. represents the iso(1)member-body(2)us(840)10045 signatures(4)sha1(1) object identifier.

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
The OID information could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNKNOWN_ALGO</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The algorithm name is not recognized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>

## -remarks

You can call the following properties to retrieve information about an initialized <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_friendlyname">FriendlyName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_name">Name</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_value">Value</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectID</a>