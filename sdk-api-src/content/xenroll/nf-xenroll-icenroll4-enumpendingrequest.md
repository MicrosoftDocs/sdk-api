---
UID: NF:xenroll.ICEnroll4.enumPendingRequest
title: ICEnroll4::enumPendingRequest (xenroll.h)
description: Enumerates pending certificate requests and retrieves a specified property from each. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","enumPendingRequest method","ICEnroll4 interface [Security]","enumPendingRequest method","ICEnroll4.enumPendingRequest","ICEnroll4::enumPendingRequest","XEPR_CADNS","XEPR_CAFRIENDLYNAME","XEPR_CANAME","XEPR_HASH","XEPR_REQUESTID","_xen_icenroll4_enumpendingrequest","enumPendingRequest","enumPendingRequest method [Security]","enumPendingRequest method [Security]","CEnroll object","enumPendingRequest method [Security]","ICEnroll4 interface","security.icenroll4_enumpendingrequest","xenroll/ICEnroll4::enumPendingRequest"]
old-location: security\icenroll4_enumpendingrequest.htm
tech.root: security
ms.assetid: 566974d1-79ec-4cbd-ae84-85e0a78edf58
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],enumPendingRequest method, ICEnroll4 interface [Security],enumPendingRequest method, ICEnroll4.enumPendingRequest, ICEnroll4::enumPendingRequest, XEPR_CADNS, XEPR_CAFRIENDLYNAME, XEPR_CANAME, XEPR_HASH, XEPR_REQUESTID, _xen_icenroll4_enumpendingrequest, enumPendingRequest, enumPendingRequest method [Security], enumPendingRequest method [Security],CEnroll object, enumPendingRequest method [Security],ICEnroll4 interface, security.icenroll4_enumpendingrequest, xenroll/ICEnroll4::enumPendingRequest
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
 - ICEnroll4::enumPendingRequest
 - xenroll/ICEnroll4::enumPendingRequest
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
 - ICEnroll4.enumPendingRequest
 - CEnroll.enumPendingRequest
---

# ICEnroll4::enumPendingRequest


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumPendingRequest</b> method enumerates pending <a href="/windows/desktop/SecGloss/c-gly">certificate requests</a> and retrieves a specified property from each.
			
This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param lIndex [in]

Specifies the ordinal position of the pending request whose property will be retrieved. Specify zero for the first request.

### -param lDesiredProperty [in]

The identifier for the property being retrieved. This parameter can be one of the following values. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XEPR_CADNS"></a><a id="xepr_cadns"></a><dl>
<dt><b>XEPR_CADNS</b></dt>
</dl>
</td>
<td width="60%">
The DNS name for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA).

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_CAFRIENDLYNAME"></a><a id="xepr_cafriendlyname"></a><dl>
<dt><b>XEPR_CAFRIENDLYNAME</b></dt>
</dl>
</td>
<td width="60%">
The display name of the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_CANAME"></a><a id="xepr_caname"></a><dl>
<dt><b>XEPR_CANAME</b></dt>
</dl>
</td>
<td width="60%">
The name of the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_HASH"></a><a id="xepr_hash"></a><dl>
<dt><b>XEPR_HASH</b></dt>
</dl>
</td>
<td width="60%">
The hash value of the request.

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_REQUESTID"></a><a id="xepr_requestid"></a><dl>
<dt><b>XEPR_REQUESTID</b></dt>
</dl>
</td>
<td width="60%">
The certificate request ID.

</td>
</tr>
</table>

### -param pvarProperty [out]

A pointer to a <b>VARIANT</b> that receives the value of the retrieved property. 




When you have finished using the <b>VARIANT</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

If the following values are specified for <i>lDesiredProperty</i>, this method returns E_NOTIMPL:<ul>
<li>XEPR_DATE</li>
<li>XEPR_V1TEMPLATENAME</li>
<li>XEPR_V2TEMPLATEOID</li>
<li>XEPR_VERSION</li>
</ul>


If you specify any other value for <i>lDesiredProperty</i> this method returns E_INVALIDARG.

<h3>VB</h3>
 Returns a <b>Variant</b> that contains a property from a pending request.

## -remarks

This method is disabled when  the Certificate Enrollment Control is executed as a scripted control.