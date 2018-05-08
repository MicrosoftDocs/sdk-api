---
UID: NF:wincrypt.CertOpenServerOcspResponse
title: CertOpenServerOcspResponse function
author: windows-driver-content
description: Opens a handle to an online certificate status protocol (OCSP) response associated with a server certificate chain.
old-location: security\certopenserverocspresponse.htm
old-project: SecCrypto
ms.assetid: c29d1972-b329-4e32-aead-a038130fb85e
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: CertOpenServerOcspResponse, CertOpenServerOcspResponse function [Security], security.certopenserverocspresponse, wincrypt/CertOpenServerOcspResponse
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
-	Crypt32.dll
api_name:
-	CertOpenServerOcspResponse
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertOpenServerOcspResponse function


## -description


The <b>CertOpenServerOcspResponse</b> function opens a handle to an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) response associated with a server certificate chain.


## -parameters




### -param pChainContext [in]

The address of a <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> structure that contains the certificate chain.


### -param dwFlags [in]

This parameter is not used and must be zero.


### -param pOpenPara

TBD




#### - pvReserved

This parameter is not used and must be <b>NULL</b>.


## -returns



Returns a handle to the OCSP response associated with a server certificate chain if successful; otherwise, <b>NULL</b>. This handle must be passed to the <a href="https://msdn.microsoft.com/6247e8ca-ba12-432f-9bf8-a6c644f253e9">CertCloseServerOcspResponse</a> function when it is no longer needed.

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error codes returned by the 
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



The <b>CertOpenServerOcspResponse</b> function tries to retrieve an initial OCSP response before it returns.
It blocks its process thread during the retrieval. The <b>CertOpenServerOcspResponse</b> function creates a background thread that prefetches time-valid OCSP responses.

The <b>CertOpenServerOcspResponse</b> function increments the reference count for the chain context represented by the <i>pChainContext</i> parameter. When you have finished using the chain context, close the returned handle by calling the <a href="https://msdn.microsoft.com/6247e8ca-ba12-432f-9bf8-a6c644f253e9">CertCloseServerOcspResponse</a> function.

The <b>CertOpenServerOcspResponse</b> function initializes configuration settings used by the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/6ccc0e85-1fa0-480c-a5b4-b21ba811e5d0">CertAddRefServerOcspResponse</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6247e8ca-ba12-432f-9bf8-a6c644f253e9">CertCloseServerOcspResponse</a>
</li>
<li>
<a href="https://msdn.microsoft.com/07476e43-db6b-4119-8d6b-41143b98744e">CertGetServerOcspResponseContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b7cdce9b-25fe-4fb9-b266-61989793699b">CertAddRefServerOcspResponseContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a07fc1e0-6f06-4336-b33c-d4d6a838b609">CertFreeServerOcspResponseContext</a>
</li>
</ul>
First, the <b>CertOpenServerOcspResponse</b> function initializes the settings based on default values in Wincrypt.h. If the function subsequently finds the registry key defined in <b>CERT_CHAIN_CONFIG_REGPATH</b>, it updates the previously initialized values with the registry values.

The following configuration setting names and default values are initialized by this function:

<ul>
<li>
<b>CERT_SRV_OCSP_RESP_MIN_VALIDITY_SECONDS_VALUE_NAME</b>

L"SrvOcspRespMinValiditySeconds"

The minimum time validity of the server OCSP response to be returned by <a href="https://msdn.microsoft.com/07476e43-db6b-4119-8d6b-41143b98744e">CertGetServerOcspResponseContext</a>. The OCSP
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




<a href="https://msdn.microsoft.com/6247e8ca-ba12-432f-9bf8-a6c644f253e9">CertCloseServerOcspResponse</a>
 

 

