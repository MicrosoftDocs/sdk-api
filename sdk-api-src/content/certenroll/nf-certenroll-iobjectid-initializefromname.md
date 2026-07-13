---
UID: NF:certenroll.IObjectId.InitializeFromName
title: IObjectId::InitializeFromName (certenroll.h)
description: Initializes the object from a CERTENROLL_OBJECTID enumeration value.
helpviewer_keywords: ["IObjectId interface [Security]","InitializeFromName method","IObjectId.InitializeFromName","IObjectId::InitializeFromName","InitializeFromName","InitializeFromName method [Security]","InitializeFromName method [Security]","IObjectId interface","certenroll/IObjectId::InitializeFromName","security.iobjectid_initializefromname_method"]
old-location: security\iobjectid_initializefromname_method.htm
tech.root: security
ms.assetid: dce84308-aecc-4841-88da-e948313b90b3
ms.date: 12/05/2018
ms.keywords: IObjectId interface [Security],InitializeFromName method, IObjectId.InitializeFromName, IObjectId::InitializeFromName, InitializeFromName, InitializeFromName method [Security], InitializeFromName method [Security],IObjectId interface, certenroll/IObjectId::InitializeFromName, security.iobjectid_initializefromname_method
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
 - IObjectId::InitializeFromName
 - certenroll/IObjectId::InitializeFromName
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
 - IObjectId.InitializeFromName
---

# IObjectId::InitializeFromName


## -description

The <b>InitializeFromName</b> method initializes the object from a  <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a> enumeration value. This method is web enabled.

## -parameters

### -param Name [in]

A <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a> enumeration value.

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

Every <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a> value is associated with an ASN.1 object identifier. For example, the value <b>XCN_OID_ECDSA_SHA1</b> is associated with a string that contains 1.2.840.10045.4.1. This is the dotted decimal representation of the iso(1)member-body(2)us(840)10045 signatures(4)sha1(1) object identifier.

The <b>InitializeFromName</b> method searches the registry for information associated with the ASN.1 object identifier. If information is found, the method internally populates a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a> structure and associates it with the object. The method also uses the local information to initialize, if possible, the display name of the object.

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

<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_friendlyname">FriendlyName</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectID</a>