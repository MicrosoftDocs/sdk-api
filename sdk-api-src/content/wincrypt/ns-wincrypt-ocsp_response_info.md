---
UID: NS:wincrypt._OCSP_RESPONSE_INFO
title: OCSP_RESPONSE_INFO (wincrypt.h)
description: Indicates the success or failure of the corresponding online certificate status protocol (OCSP) request. For successful requests, it contains the type and value of response information.
helpviewer_keywords: ["*POCSP_RESPONSE_INFO","OCSP_INTERNAL_ERROR_RESPONSE","OCSP_MALFORMED_REQUEST_RESPONSE","OCSP_RESPONSE_INFO","OCSP_RESPONSE_INFO structure [Security]","OCSP_SIG_REQUIRED_RESPONSE","OCSP_SUCCESSFUL_RESPONSE","OCSP_TRY_LATER_RESPONSE","OCSP_UNAUTHORIZED_RESPONSE","POCSP_RESPONSE_INFO","POCSP_RESPONSE_INFO structure pointer [Security]","security.ocsp_response_info","szOID_PKIX_OCSP_BASIC_SIGNED_RESPONSE","wincrypt/OCSP_RESPONSE_INFO","wincrypt/POCSP_RESPONSE_INFO"]
old-location: security\ocsp_response_info.htm
tech.root: security
ms.assetid: e3829739-dd10-4886-8048-cd1b1b712d56
ms.date: 12/05/2018
ms.keywords: '*POCSP_RESPONSE_INFO, OCSP_INTERNAL_ERROR_RESPONSE, OCSP_MALFORMED_REQUEST_RESPONSE, OCSP_RESPONSE_INFO, OCSP_RESPONSE_INFO structure [Security], OCSP_SIG_REQUIRED_RESPONSE, OCSP_SUCCESSFUL_RESPONSE, OCSP_TRY_LATER_RESPONSE, OCSP_UNAUTHORIZED_RESPONSE, POCSP_RESPONSE_INFO, POCSP_RESPONSE_INFO structure pointer [Security], security.ocsp_response_info, szOID_PKIX_OCSP_BASIC_SIGNED_RESPONSE, wincrypt/OCSP_RESPONSE_INFO, wincrypt/POCSP_RESPONSE_INFO'
req.header: wincrypt.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OCSP_RESPONSE_INFO, *POCSP_RESPONSE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OCSP_RESPONSE_INFO
 - wincrypt/_OCSP_RESPONSE_INFO
 - POCSP_RESPONSE_INFO
 - wincrypt/POCSP_RESPONSE_INFO
 - OCSP_RESPONSE_INFO
 - wincrypt/OCSP_RESPONSE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - OCSP_RESPONSE_INFO
---

# OCSP_RESPONSE_INFO structure


## -description

The <b>OCSP_RESPONSE_INFO</b> structure indicates the success or failure of the corresponding <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) request. For successful requests, it contains the type and value of response information.

## -struct-fields

### -field dwStatus

A value that indicates the processing status of the corresponding request. If the status is anything other than <b>OCSP_SUCCESSFUL_RESPONSE</b>, <b>pszObjId</b> and <b>Value</b> are not set.


This member can be one of the following possible values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OCSP_SUCCESSFUL_RESPONSE"></a><a id="ocsp_successful_response"></a><dl>
<dt><b>OCSP_SUCCESSFUL_RESPONSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The response has valid confirmations.

</td>
</tr>
<tr>
<td width="40%"><a id="OCSP_MALFORMED_REQUEST_RESPONSE"></a><a id="ocsp_malformed_request_response"></a><dl>
<dt><b>OCSP_MALFORMED_REQUEST_RESPONSE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The request received does not conform to OCSP syntax.

</td>
</tr>
<tr>
<td width="40%"><a id="OCSP_INTERNAL_ERROR_RESPONSE"></a><a id="ocsp_internal_error_response"></a><dl>
<dt><b>OCSP_INTERNAL_ERROR_RESPONSE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The responder encountered an internal error. The request should be resent to a different responder.

</td>
</tr>
<tr>
<td width="40%"><a id="OCSP_TRY_LATER_RESPONSE"></a><a id="ocsp_try_later_response"></a><dl>
<dt><b>OCSP_TRY_LATER_RESPONSE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The responder service is operational but temporarily unable to respond.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
This value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="OCSP_SIG_REQUIRED_RESPONSE"></a><a id="ocsp_sig_required_response"></a><dl>
<dt><b>OCSP_SIG_REQUIRED_RESPONSE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Before the responder service can respond, it requires that the client sign the request.

</td>
</tr>
<tr>
<td width="40%"><a id="OCSP_UNAUTHORIZED_RESPONSE"></a><a id="ocsp_unauthorized_response"></a><dl>
<dt><b>OCSP_UNAUTHORIZED_RESPONSE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The client is not authorized to request a response from this responder service.

</td>
</tr>
</table>

### -field pszObjId

A pointer to a string that identifies the type of data in <b>Value</b>.


The following table lists possible values for <b>pszObjId</b>.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_PKIX_OCSP_BASIC_SIGNED_RESPONSE"></a><a id="szoid_pkix_ocsp_basic_signed_response"></a><a id="SZOID_PKIX_OCSP_BASIC_SIGNED_RESPONSE"></a><dl>
<dt><b>szOID_PKIX_OCSP_BASIC_SIGNED_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
1.3.6.1.5.5.7.48.1.1

</td>
</tr>
</table>

### -field Value

An array of bytes that contain data encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER), as specified by <b>pszObjId</b>.

## -remarks

OCSP applications can encode or decode this structure by using <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_signed_response_info">OCSP_BASIC_SIGNED_RESPONSE_INFO</a>



<a href="https://www.ietf.org/rfc/rfc2560.txt">RFC 2560  Online Certificate Status Protocol</a>