---
UID: NF:certenroll.ICertificatePolicy.Initialize
title: ICertificatePolicy::Initialize (certenroll.h)
description: Initializes the object from an object identifier (OID).
helpviewer_keywords: ["ICertificatePolicy interface [Security]","Initialize method","ICertificatePolicy.Initialize","ICertificatePolicy::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertificatePolicy interface","certenroll/ICertificatePolicy::Initialize","security.icertificatepolicy_initialize_method"]
old-location: security\icertificatepolicy_initialize_method.htm
tech.root: security
ms.assetid: 995b344b-ed1f-47e4-a7c6-0d638ed9ec23
ms.date: 12/05/2018
ms.keywords: ICertificatePolicy interface [Security],Initialize method, ICertificatePolicy.Initialize, ICertificatePolicy::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertificatePolicy interface, certenroll/ICertificatePolicy::Initialize, security.icertificatepolicy_initialize_method
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
 - ICertificatePolicy::Initialize
 - certenroll/ICertificatePolicy::Initialize
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
 - ICertificatePolicy.Initialize
---

# ICertificatePolicy::Initialize


## -description

The <b>Initialize</b> method initializes the object from an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

## -parameters

### -param pValue [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that represents the OID.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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

You must use an initialized <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object when calling this method. All of the  <b>IObjectId</b> initialization methods search  the registry and static memory on the local computer and Active Directory on the domain server for the first OID that matches the specified initialization parameters. You can retrieve the OID by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertificatepolicy-get_objectid">ObjectId</a> property.

When you call the <b>Initialize</b> method, an empty <a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifiers">IPolicyQualifiers</a> object is created. You can retrieve the object by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertificatepolicy-get_policyqualifiers">PolicyQualifiers</a> property. You can use the object to define policy qualifiers if you are creating a <b>CertificatePolicies</b> extension.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a>