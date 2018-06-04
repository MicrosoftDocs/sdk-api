---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _OCSP_RESPONSE_INFO structure


## -description


The <b>OCSP_RESPONSE_INFO</b> structure indicates the success or failure of the corresponding <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) request. For successful requests, it contains the type and value of response information.


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

An array of bytes that contain data encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER), as specified by <b>pszObjId</b>.


## -remarks



OCSP applications can encode or decode this structure by using <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.




## -see-also




<a href="https://msdn.microsoft.com/4b88a946-030f-490a-b46a-c42507e1268d">OCSP_BASIC_SIGNED_RESPONSE_INFO</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=91156">RFC 2560  Online Certificate Status Protocol</a>
 

 

