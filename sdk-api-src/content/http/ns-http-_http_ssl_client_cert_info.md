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

# _HTTP_SSL_CLIENT_CERT_INFO structure


## -description


The 
<b>HTTP_SSL_CLIENT_CERT_INFO</b> structure contains data about a Secure Sockets Layer (SSL) client certificate that can be used to determine whether the certificate is valid.


## -struct-fields




### -field CertFlags

Flags that indicate whether the certificate is valid. The possible values for this member are 
a <a href="https://msdn.microsoft.com/b5f8ed5c-797a-46fa-8a73-a054ecc50265">SSPI Status Code</a> returned from SSPI or one of the following flags from the <b>dwError</b> member of the <a href="https://msdn.microsoft.com/599a09b6-fe9e-4489-99ae-8a88fa78a660">CERT_CHAIN_POLICY_STATUS</a> structure:

<a id="CERT_E_EXPIRED"></a>
<a id="cert_e_expired"></a>


#### CERT_E_EXPIRED

<a id="CERT_E_UNTRUSTEDCA"></a>
<a id="cert_e_untrustedca"></a>


#### CERT_E_UNTRUSTEDCA

<a id="CERT_E_WRONG_USAGE"></a>
<a id="cert_e_wrong_usage"></a>


#### CERT_E_WRONG_USAGE

<a id="CERT_E_UNTRUSTEDROOT"></a>
<a id="cert_e_untrustedroot"></a>


#### CERT_E_UNTRUSTEDROOT

<a id="CERT_E_REVOKED"></a>
<a id="cert_e_revoked"></a>


#### CERT_E_REVOKED

<a id="CERT_E_CN_NO_MATCH"></a>
<a id="cert_e_cn_no_match"></a>


#### CERT_E_CN_NO_MATCH


### -field CertEncodedSize

The size, in bytes, of the certificate.


### -field pCertEncoded

A pointer to the actual certificate.


### -field Token

A handle to an access token. If the HTTP_SERVICE_CONFIG_SSL_FLAG_USE_DS_MAPPER flag is set using the 
<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a> function, and the client certificate was successfully mapped to an operating-system user account, then this member contains the handle to a valid 
<a href="https://msdn.microsoft.com/350159c9-2399-427a-ba44-c897a9664299">access token</a>. When the 
<b>HTTP_SSL_CLIENT_CERT_INFO</b> structure is no longer required, release this token explicitly by closing the handle.


### -field CertDeniedByMapper

Reserved.


## -remarks



An 
<b>HTTP_SSL_CLIENT_CERT_INFO</b> structure is pointed to by the <b>pClientCertInfo</b> member of the 
<a href="https://msdn.microsoft.com/35aac36d-87a1-45b2-acb1-6969c992d0cf">HTTP_SSL_INFO</a> structure, and is used by the 
<a href="https://msdn.microsoft.com/f0cf7b77-2868-4142-a663-32d6ea7df9e9">HttpReceiveClientCertificate</a> function to return data about the client certificate through the <i>pSslClientCertInfo</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/e38f7a05-f966-4853-be3b-5cdbf224719e">HTTP Server API Version 1.0 Structures</a>



<a href="https://msdn.microsoft.com/35aac36d-87a1-45b2-acb1-6969c992d0cf">HTTP_SSL_INFO</a>



<a href="https://msdn.microsoft.com/f0cf7b77-2868-4142-a663-32d6ea7df9e9">HttpReceiveClientCertificate</a>
 

 

