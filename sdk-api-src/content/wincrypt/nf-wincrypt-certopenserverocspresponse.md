---
UID: NF:wincrypt.CertOpenServerOcspResponse
title: CertOpenServerOcspResponse function (wincrypt.h)
description: Opens a handle to an online certificate status protocol (OCSP) response associated with a server certificate chain.
helpviewer_keywords: ["CertOpenServerOcspResponse","CertOpenServerOcspResponse function [Security]","security.certopenserverocspresponse","wincrypt/CertOpenServerOcspResponse"]
old-location: security\certopenserverocspresponse.htm
tech.root: security
ms.assetid: c29d1972-b329-4e32-aead-a038130fb85e
ms.date: 12/05/2018
ms.keywords: CertOpenServerOcspResponse, CertOpenServerOcspResponse function [Security], security.certopenserverocspresponse, wincrypt/CertOpenServerOcspResponse
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertOpenServerOcspResponse
 - wincrypt/CertOpenServerOcspResponse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertOpenServerOcspResponse
---

# CertOpenServerOcspResponse function


## -description

The <b>CertOpenServerOcspResponse</b> function opens a handle to an <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) response associated with a server certificate chain.

## -parameters

### -param pChainContext [in]

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CERT_CHAIN_CONTEXT</a> structure that contains the certificate chain.

### -param dwFlags [in]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><a id="0"></a><dl>
<dt><b>0</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
This API will try to retrieve an initial OCSP response before returning, which means it will block during the retrieval.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SERVER_OCSP_RESPONSE_ASYNC_FLAG"></a><a id="CERT_SERVER_OCSP_RESPONSE_ASYNC_FLAG"></a><dl>
<dt><b>CERT_SERVER_OCSP_RESPONSE_ASYNC_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Set this flag to return immediately without making the initial synchronous retrieval.
	
</td>
</tr>
</table>

### -param pOpenPara

This parameter is not used and must be <b>NULL</b>.

## -returns

Returns a handle to the OCSP response associated with a server certificate chain if successful; otherwise, <b>NULL</b>. This handle must be passed to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcloseserverocspresponse">CertCloseServerOcspResponse</a> function when it is no longer needed.

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error codes returned by the 
		       <b>GetLastError</b> function include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_IN_REVOCATION_DATABASE</b></dt>
</dl>
</td>
<td width="60%">
The end certificate does not contain an OCSP authority information access (AIA) URL.

</td>
</tr>
</table>

## -remarks

When the <b>dwFlags</b> is set to 0, the <b>CertOpenServerOcspResponse</b> function tries to retrieve an initial OCSP response before it returns.
It blocks its process thread during the retrieval. The <b>CertOpenServerOcspResponse</b> function creates a background thread that prefetches time-valid OCSP responses. If unable to successfully retrieve the first OCSP response, a non-NULL handle will still be returned if not one of the error cases mentioned above.

When the <b>dwFlags</b> is set to 1 or <b>CERT_SERVER_OCSP_RESPONSE_ASYNC_FLAG</b>, the <b>CertOpenServerOcspResponse</b> function will return immediately without making the initial synchronous retrieval.

The <b>CertOpenServerOcspResponse</b> function increments the reference count for the chain context represented by the <i>pChainContext</i> parameter. When you have finished using the chain context, close the returned handle by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcloseserverocspresponse">CertCloseServerOcspResponse</a> function.

The <b>CertOpenServerOcspResponse</b> function initializes configuration settings used by the following functions:

<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddrefserverocspresponse">CertAddRefServerOcspResponse</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcloseserverocspresponse">CertCloseServerOcspResponse</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetserverocspresponsecontext">CertGetServerOcspResponseContext</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddrefserverocspresponsecontext">CertAddRefServerOcspResponseContext</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreeserverocspresponsecontext">CertFreeServerOcspResponseContext</a>
</li>
</ul>
First, the <b>CertOpenServerOcspResponse</b> function initializes the settings based on default values in Wincrypt.h. If the function subsequently finds the registry key defined in <b>CERT_CHAIN_CONFIG_REGPATH</b>, it updates the previously initialized values with the registry values.

The following configuration setting names and default values are initialized by this function:

<ul>
<li>
<b>CERT_SRV_OCSP_RESP_MIN_VALIDITY_SECONDS_VALUE_NAME</b>

L"SrvOcspRespMinValiditySeconds"

The minimum time validity of the server OCSP response to be returned by <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetserverocspresponsecontext">CertGetServerOcspResponseContext</a>. The OCSP
response validity must be sufficiently long that the client treats it as time valid.

</li>
<li>
<b>CERT_SRV_OCSP_RESP_MIN_VALIDITY_SECONDS_DEFAULT</b>

(10 × 60)

10 minutes.

</li>
<li>
<b>CERT_SRV_OCSP_RESP_URL_RETRIEVAL_TIMEOUT_MILLISECONDS_VALUE_NAME</b>

L"SrvOcspRespUrlRetrievalTimeoutMilliseconds"

This is the maximum time before an OCSP response prefetch wire URL retrieval times out.

</li>
<li>
<b>CERT_SRV_OCSP_RESP_URL_RETRIEVAL_TIMEOUT_MILLISECONDS_DEFAULT</b>

(15 × 1000)

15 seconds.

</li>
<li>
<b>CERT_SRV_OCSP_RESP_MAX_BEFORE_NEXT_UPDATE_SECONDS_VALUE_NAME</b>

L"SrvOcspRespMaxBeforeNextUpdateSeconds"

This is the maximum number of seconds to perform a server OCSP response
prefetch retrieval before the NextUpdate date of an OCSP response. The
server OCSP response thread waits until the current time is greater than or equal to the NextUpdate date minus this number of seconds to perform a prefetch retrieval.

</li>
<li>
<b>CERT_SRV_OCSP_RESP_MAX_BEFORE_NEXT_UPDATE_SECONDS_DEFAULT</b>

(4 ×60 × 60)

4 hours.

</li>
<li>
<b>CERT_SRV_OCSP_RESP_MIN_BEFORE_NEXT_UPDATE_SECONDS_VALUE_NAME</b>

L"SrvOcspRespMinBeforeNextUpdateSeconds"

This is the minimum number of seconds to perform a server OCSP response
prefetch retrieval before the NextUpdate date of an OCSP response. If the current time is greater than or equal to the NextUpdate date minus this number of seconds, the server OCSP response thread waits until
after the NextUpdate date plus the  <b>CERT_SRV_OCSP_RESP_MIN_AFTER_NEXT_UPDATE_SECONDS_VALUE_NAME</b> number of seconds before it performs a prefetch retrieval.

</li>
<li>
<b>CERT_SRV_OCSP_RESP_MIN_BEFORE_NEXT_UPDATE_SECONDS_DEFAULT</b>

(2 × 60)

2 minutes.

</li>
<li>
<b>CERT_SRV_OCSP_RESP_MIN_AFTER_NEXT_UPDATE_SECONDS_VALUE_NAME</b>

L"SrvOcspRespMinAfterNextUpdateSeconds"

This is the minimum number of seconds to perform a server OCSP response
prefetch retrieval after the NextUpdate date of an OCSP response. When the current time is greater than the NextUpdate date minus the <b>CERT_SRV_OCSP_RESP_MIN_BEFORE_NEXT_UPDATE_SECONDS_VALUE_NAME</b> number of seconds but less than the NextUpdate date, the server OCSP response thread waits this number of seconds after the NextUpdate date to perform a prefetch retrieval.

</li>
<li>
<b>CERT_SRV_OCSP_RESP_MIN_AFTER_NEXT_UPDATE_SECONDS_DEFAULT</b>

(1 × 60)

1 minute.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcloseserverocspresponse">CertCloseServerOcspResponse</a>
