---
UID: NF:xenroll.ICEnroll4.addCertTypeToRequestEx
title: ICEnroll4::addCertTypeToRequestEx (xenroll.h)
description: Adds a certificate template (or &quot;certificate type&quot;) to a request.
helpviewer_keywords: ["CEnroll object [Security]","addCertTypeToRequestEx method","ICEnroll4 interface [Security]","addCertTypeToRequestEx method","ICEnroll4.addCertTypeToRequestEx","ICEnroll4::addCertTypeToRequestEx","XECT_EXTENSION_V1","XECT_EXTENSION_V2","_xen_icenroll4_addcerttypetorequestex","addCertTypeToRequestEx","addCertTypeToRequestEx method [Security]","addCertTypeToRequestEx method [Security]","CEnroll object","addCertTypeToRequestEx method [Security]","ICEnroll4 interface","security.icenroll4_addcerttypetorequestex","xenroll/ICEnroll4::addCertTypeToRequestEx"]
old-location: security\icenroll4_addcerttypetorequestex.htm
tech.root: security
ms.assetid: bde35e01-8b26-44f7-828e-e8313a2b5a12
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],addCertTypeToRequestEx method, ICEnroll4 interface [Security],addCertTypeToRequestEx method, ICEnroll4.addCertTypeToRequestEx, ICEnroll4::addCertTypeToRequestEx, XECT_EXTENSION_V1, XECT_EXTENSION_V2, _xen_icenroll4_addcerttypetorequestex, addCertTypeToRequestEx, addCertTypeToRequestEx method [Security], addCertTypeToRequestEx method [Security],CEnroll object, addCertTypeToRequestEx method [Security],ICEnroll4 interface, security.icenroll4_addcerttypetorequestex, xenroll/ICEnroll4::addCertTypeToRequestEx
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll4::addCertTypeToRequestEx
 - xenroll/ICEnroll4::addCertTypeToRequestEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.addCertTypeToRequestEx
 - CEnroll.addCertTypeToRequestEx
---

# ICEnroll4::addCertTypeToRequestEx


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addCertTypeToRequestEx</b>  method, like the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll2-addcerttypetorequest">addCertTypeToRequest</a> method, adds a certificate template (or "certificate type") to a request. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

This method is associated with the Certificate Services enterprise 
<a href="/windows/desktop/SecCrypto/policy-modules">policy module</a>. This method is specialized, and its use is not recommended for most applications. This version can add a V@ template extension into a request.

## -parameters

### -param lType [in]

Indicates the version type of the template extension. This can be either of the following values: 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XECT_EXTENSION_V1"></a><a id="xect_extension_v1"></a><dl>
<dt><b>XECT_EXTENSION_V1</b></dt>
</dl>
</td>
<td width="60%">
Uses a version 1 extension

</td>
</tr>
<tr>
<td width="40%"><a id="XECT_EXTENSION_V2"></a><a id="xect_extension_v2"></a><dl>
<dt><b>XECT_EXTENSION_V2</b></dt>
</dl>
</td>
<td width="60%">
Uses a version 2 extension

</td>
</tr>
</table>

### -param bstrOIDOrName [in]

The certificate template fully qualified name which is being added to the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. This value is interpreted by the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>.

### -param lMajorVersion [in]

Sets the major version of the template. This parameter is ignored if <i>lFlag</i> is XECT_EXTENSION_V!.

### -param fMinorVersion [in]

Indicates whether a minor version of the template is used. This parameter is ignored if <i>lFlag</i> is XECT_EXTENSION_V!.

### -param lMinorVersion [in]

Sets the minor version of the template. This parameter is ignored if <i>lFlag</i> is XECT_EXTENSION_V1 or if <i>fMinorVersion</i> is <b>FALSE</b>.

## -returns

<h3>VB</h3>
 The return value is an <b>HRESULT</b>, with <b>S_OK</b> returned if the call is successful.

## -remarks

This method supports only the new request method, 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll4-createrequest">createRequest</a>. It does not support the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a> method.

This method can be called multiple times to establish multiple certificate templates for the request.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll2-addcerttypetorequest">ICEnroll2::addCertTypeToRequest</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll4-createrequest">ICEnroll4::createRequest</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">ICEnroll::createPKCS10</a>