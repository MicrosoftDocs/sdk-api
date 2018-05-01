---
UID: NF:wincrypt.CryptGetTimeValidObject
title: CryptGetTimeValidObject function
author: windows-driver-content
description: Retrieves a CRL, an OCSP response, or CTL object that is valid within a given context and time.
old-location: security\cryptgettimevalidobject.htm
old-project: SecCrypto
ms.assetid: dd639b43-1560-4e9f-a778-9e20484ae012
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CRYPT_ACCUMULATIVE_TIMEOUT, CRYPT_CACHE_ONLY_RETRIEVAL, CRYPT_CHECK_FRESHNESS_TIME_VALIDITY, CRYPT_DONT_CHECK_TIME_VALIDITY, CRYPT_DONT_VERIFY_SIGNATURE, CRYPT_KEEP_TIME_VALID, CRYPT_OCSP_ONLY_RETRIEVAL, CRYPT_WIRE_ONLY_RETRIEVAL, CryptGetTimeValidObject, CryptGetTimeValidObject function [Security], TIME_VALID_OID_GET_CRL, TIME_VALID_OID_GET_CRL_FROM_CERT, TIME_VALID_OID_GET_CTL, TIME_VALID_OID_GET_FRESHEST_CRL_FROM_CERT, TIME_VALID_OID_GET_FRESHEST_CRL_FROM_CRL, security.cryptgettimevalidobject, wincrypt/CryptGetTimeValidObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Cryptnet.dll
api_name:
-	CryptGetTimeValidObject
product: Windows
targetos: Windows
req.lib: Cryptnet.lib
req.dll: Cryptnet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptGetTimeValidObject function


## -description


The <b>CryptGetTimeValidObject</b> function retrieves a CRL, an OCSP response, or CTL object that is valid within a given context and time.


## -parameters




### -param pszTimeValidOid [in]

A pointer to an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) that identifies the object being requested. If the <a href="_win32_hiword_cpp">HIWORD</a> of the <i>pszTimeValidOid</i> parameter is zero, the <a href="_win32_loword_cpp">LOWORD</a> specifies the integer identifier for the type of the specified structure. 


This parameter can be one of the following values. For information about how these values affect the pvPara parameter, see the heading "For the pvPara parameter" in the Meaning column.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TIME_VALID_OID_GET_CTL"></a><a id="time_valid_oid_get_ctl"></a><dl>
<dt><b>TIME_VALID_OID_GET_CTL</b></dt>
<dt>((LPCSTR)1)</dt>
</dl>
</td>
<td width="60%">
Provides a certificate trust list (CTL) based on a URL obtained from the <b>NextUpdateLocation</b> property or extension of the current CTL context.

For the pvPara parameter: A pointer to a <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">PCCTL_CONTEXT</a> that represents the current certificate trust list.

</td>
</tr>
<tr>
<td width="40%"><a id="TIME_VALID_OID_GET_CRL"></a><a id="time_valid_oid_get_crl"></a><dl>
<dt><b>TIME_VALID_OID_GET_CRL</b></dt>
</dl>
</td>
<td width="60%">
This value is reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="TIME_VALID_OID_GET_CRL_FROM_CERT"></a><a id="time_valid_oid_get_crl_from_cert"></a><dl>
<dt><b>TIME_VALID_OID_GET_CRL_FROM_CERT</b></dt>
<dt>((LPCSTR)3)</dt>
</dl>
</td>
<td width="60%">
Provides a CRL based on information obtained from the CRL distribution points extension of the current certificate context.

For the pvPara parameter: A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">PCCERT_CONTEXT</a> that represents the subject certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="TIME_VALID_OID_GET_FRESHEST_CRL_FROM_CERT"></a><a id="time_valid_oid_get_freshest_crl_from_cert"></a><dl>
<dt><b>TIME_VALID_OID_GET_FRESHEST_CRL_FROM_CERT</b></dt>
<dt>((LPCSTR)4)</dt>
</dl>
</td>
<td width="60%">
Provides a delta CRL based on information obtained from the freshest CRL extension of the current certificate context.

For the pvPara parameter: A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">PCCERT_CONTEXT</a> that represents the subject certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="TIME_VALID_OID_GET_FRESHEST_CRL_FROM_CRL"></a><a id="time_valid_oid_get_freshest_crl_from_crl"></a><dl>
<dt><b>TIME_VALID_OID_GET_FRESHEST_CRL_FROM_CRL</b></dt>
<dt>((LPCSTR)5)</dt>
</dl>
</td>
<td width="60%">
Provides a delta CRL based on information obtained from the freshest CRL extension of the current CRL context.

For the pvPara parameter: A pointer to a <a href="https://msdn.microsoft.com/e88781f0-8474-47d3-8218-de95f7eadf04">PCCERT_CRL_CONTEXT_PAIR</a> that represents the subject certificate and its base CRL.

</td>
</tr>
</table>
 


### -param pvPara [in]

A structure determined by the value of <i>pszTimeValidOid</i>. For details, see the description for the <i>pszTimeValidOid</i> parameter.


### -param pIssuer [in]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> containing the issuer's certificate.


### -param pftValidFor [in, optional]

A pointer to an optional <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure version of the current system time or a freshness time from the current context.


### -param dwFlags [in]

A value that determines various retrieval factors such as time-out, source, and validity checks.


The following table lists possible values for the <i>dwFlags</i> parameter.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACCUMULATIVE_TIMEOUT"></a><a id="crypt_accumulative_timeout"></a><dl>
<dt><b>CRYPT_ACCUMULATIVE_TIMEOUT</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Use the cumulative time-out registry setting of the client computer for revocation URL retrievals.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_CACHE_ONLY_RETRIEVAL"></a><a id="crypt_cache_only_retrieval"></a><dl>
<dt><b>CRYPT_CACHE_ONLY_RETRIEVAL</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Retrieve the encoded bits from the client URL cache only. Do not use the wire to retrieve the URL.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_CHECK_FRESHNESS_TIME_VALIDITY"></a><a id="crypt_check_freshness_time_validity"></a><dl>
<dt><b>CRYPT_CHECK_FRESHNESS_TIME_VALIDITY</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Check if the ThisUpdate property or extension of the current context is greater than or equal to the <i>ftValidFor</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DONT_CHECK_TIME_VALIDITY"></a><a id="crypt_dont_check_time_validity"></a><dl>
<dt><b>CRYPT_DONT_CHECK_TIME_VALIDITY</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Do not perform time validity check. Use this to retrieve a more recent base CRL over the wire or to bypass time validity check during a cache retrieval. When this flag is set, <i>pftValidFor</i> can be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DONT_VERIFY_SIGNATURE"></a><a id="crypt_dont_verify_signature"></a><dl>
<dt><b>CRYPT_DONT_VERIFY_SIGNATURE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Do not perform signature verification. Use this when verification of the retrieved object will be performed outside of this function or to force a replacement of a retrieved cache entry with a new cache entry for the object.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_KEEP_TIME_VALID"></a><a id="crypt_keep_time_valid"></a><dl>
<dt><b>CRYPT_KEEP_TIME_VALID</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
This value is reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OCSP_ONLY_RETRIEVAL"></a><a id="crypt_ocsp_only_retrieval"></a><dl>
<dt><b>CRYPT_OCSP_ONLY_RETRIEVAL</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
Retrieves the time valid object from an OCSP responder service only based on Authority Information Access URLs in the current context. The <a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a> function sets this flag when it is called with the <i>dwFlags</i> parameter set to CERT_VERIFY_REV_SERVER_OCSP_FLAG.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_WIRE_ONLY_RETRIEVAL"></a><a id="crypt_wire_only_retrieval"></a><dl>
<dt><b>CRYPT_WIRE_ONLY_RETRIEVAL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Retrieves the encoded bits from the wire only. Does not use the URL cache.

</td>
</tr>
</table>
 


### -param dwTimeout [in]

A value, in milliseconds, that specifies when to terminate an URL retrieval attempt that has not returned a result.


### -param ppvObject [out, optional]

A pointer to an address for the returned object. The return type can be one of the supported types shown in the <i>pszObjectOid</i> parameter of the <a href="https://msdn.microsoft.com/2e205f97-be9b-4358-ba22-d475b6a250b7">CryptRetrieveObjectByUrl</a> function.


### -param pCredentials [in, optional]

A pointer to an optional <a href="https://msdn.microsoft.com/d28b2f52-3258-44ad-a3ab-0743d3afcd62">CRYPT_CREDENTIALS</a> structure used to access the URL. The only type of credentials currently supported are user name and password credentials.


### -param pExtraInfo [in, out, optional]

A pointer to an optional <a href="https://msdn.microsoft.com/3de595f9-c922-4c8f-8328-819e91a2997c">CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO</a> structure that contains extra information about the cache entry for an object.


## -returns




						If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

 Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The caller specified <b>TIME_VALID_OID_GET_CRL</b> for the <i>pszTimeValidOid</i> parameter. This OID is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_IN_REVOCATION_DATABASE</b></dt>
</dl>
</td>
<td width="60%">
The caller set the CRYPT_OCSP_ONLY_RETRIEVAL flag and the context includes a non-OCSP URL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The function failed to retrieve a CRL from a certificate context or retrieve a CTL, and it failed to copy any URLs from a cache entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate memory for an internal array operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The caller did not set the <b>CRYPT_CACHE_ONLY_RETRIEVAL</b> flag and is not connected to the Internet.

</td>
</tr>
</table>
 




## -remarks



The Cryptnet dynamic link library implements a time valid object (TVO) cache that is used to support the <b>CryptGetTimeValidObject</b> function. The cache is used by a process-global TVO agent where each cache entry consists of the following information.

<ul>
<li>Origin Identifier</li>
<li>Context OID</li>
<li>Context</li>
<li>Retrieval URL</li>
<li>Expire Time</li>
<li>Offline URL Time Information</li>
</ul>
The TVO agent supports retrieval of TVO objects on-demand or by auto-update.



