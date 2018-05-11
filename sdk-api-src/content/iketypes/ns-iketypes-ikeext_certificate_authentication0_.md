---
UID: NS:iketypes.IKEEXT_CERTIFICATE_AUTHENTICATION0_
title: IKEEXT_CERTIFICATE_AUTHENTICATION0_
author: windows-driver-content
description: Is used to specify various parameters for authentication with certificates.
old-location: fwp\ikeext_certificate_authentication0.htm
old-project: FWP
ms.assetid: e9f9625d-b68b-4b7d-a587-39dac04dd991
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IKEEXT_CERTIFICATE_AUTHENTICATION0, IKEEXT_CERTIFICATE_AUTHENTICATION0 structure [Filtering], IKEEXT_CERTIFICATE_AUTHENTICATION0_, IKEEXT_CERT_AUTH_ALLOW_HTTP_CERT_LOOKUP, IKEEXT_CERT_AUTH_DISABLE_SSL_CERT_VALIDATION, IKEEXT_CERT_AUTH_ENABLE_CRL_CHECK_STRONG, IKEEXT_CERT_AUTH_FLAG_DISABLE_CRL_CHECK, IKEEXT_CERT_AUTH_FLAG_SSL_ONE_WAY, IKEEXT_CERT_AUTH_URL_CONTAINS_BUNDLE, fwp.ikeext_certificate_authentication0, iketypes/IKEEXT_CERTIFICATE_AUTHENTICATION0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IKEEXT_CERTIFICATE_AUTHENTICATION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iketypes.h
api_name:
-	IKEEXT_CERTIFICATE_AUTHENTICATION0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_CERTIFICATE_AUTHENTICATION0_ structure


## -description


The <b>IKEEXT_CERTIFICATE_AUTHENTICATION0</b> structure is used to specify various parameters for authentication with certificates.<div class="alert"><b>Note</b>  <b>IKEEXT_CERTIFICATE_AUTHENTICATION0</b> is the specific implementation of IKEEXT_CERTIFICATE_AUTHENTICATION used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/45325f89-b5c9-4f8c-b9b0-4f0b01b34aab">IKEEXT_CERTIFICATE_AUTHENTICATION1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/39332187-6562-4f58-9284-e2aaccf1489b">IKEEXT_CERTIFICATE_AUTHENTICATION2</a> is available.</div>
<div> </div>



## -struct-fields




### -field inboundConfigType

Certificate configuration type for inbound peer certificate verification.

See <a href="https://msdn.microsoft.com/b137e27b-c361-4fd2-9b3b-5c2b364576d4">IKEEXT_CERT_CONFIG_TYPE</a> for more information.


### -field inboundRootArraySize

Number of elements in the <b>inboundRootArray</b> member.

Available when <b>inboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST</b>.


### -field inboundRootArray

Explicit trust list for verifying the peer certificate chain.

Available when <b>inboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST</b>.

See <a href="https://msdn.microsoft.com/820da66b-670e-490e-bba4-c2b0afb6dfd1">IKEEXT_CERT_ROOT_CONFIG0</a> for more information.


### -field inboundEnterpriseStoreConfig

Enterprise store configuration for verifying the peer certificate chain.

Available when <b>inboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_ENTERPRISE_STORE</b>.

See <a href="https://msdn.microsoft.com/820da66b-670e-490e-bba4-c2b0afb6dfd1">IKEEXT_CERT_ROOT_CONFIG0</a> for more information.


### -field inboundTrustedRootStoreConfig

Trusted root store configuration for verifying the peer certificate chain.

Available when <b>inboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE</b>.

See <a href="https://msdn.microsoft.com/820da66b-670e-490e-bba4-c2b0afb6dfd1">IKEEXT_CERT_ROOT_CONFIG0</a> for more information.


### -field outboundConfigType

Certificate configuration type for outbound local certificate verification.

See <a href="https://msdn.microsoft.com/b137e27b-c361-4fd2-9b3b-5c2b364576d4">IKEEXT_CERT_CONFIG_TYPE</a> for more information.


### -field outboundRootArraySize

Number of elements in the <b>outboundRootArray</b> member.

Available when <b>outboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST</b>.


### -field outboundRootArray

Explicit trust list for selecting a certificate chain to send to the peer.

Available when <b>outboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST</b>.

See <a href="https://msdn.microsoft.com/820da66b-670e-490e-bba4-c2b0afb6dfd1">IKEEXT_CERT_ROOT_CONFIG0</a> for more information.


### -field outboundEnterpriseStoreConfig

Enterprise store configuration for selecting  the certificate chain.

Available when <b>outboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_ENTERPRISE_STORE</b>.

See <a href="https://msdn.microsoft.com/820da66b-670e-490e-bba4-c2b0afb6dfd1">IKEEXT_CERT_ROOT_CONFIG0</a> for more information.


### -field outboundTrustedRootStoreConfig

Trusted root store configuration for selecting the certificate chain.

Available when <b>outboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_ROOT_STORE</b>.

See <a href="https://msdn.microsoft.com/820da66b-670e-490e-bba4-c2b0afb6dfd1">IKEEXT_CERT_ROOT_CONFIG0</a> for more information.


### -field flags

A combination of the following values that specifies  the certificate authentication characteristics.

<table>
<tr>
<th>IKE/AuthIP certificate authentication flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_AUTH_FLAG_SSL_ONE_WAY"></a><a id="ikeext_cert_auth_flag_ssl_one_way"></a><dl>
<dt><b>IKEEXT_CERT_AUTH_FLAG_SSL_ONE_WAY</b></dt>
</dl>
</td>
<td width="60%">
Enable SSL one way authentication.

 Applicable only to AuthIP.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_AUTH_FLAG_DISABLE_CRL_CHECK__"></a><a id="ikeext_cert_auth_flag_disable_crl_check__"></a><dl>
<dt><b>IKEEXT_CERT_AUTH_FLAG_DISABLE_CRL_CHECK  </b></dt>
</dl>
</td>
<td width="60%">
Disable CRL checking. By default weak CRL checking is enabled. Weak checking 
means that a certificate will be rejected if and only if CRL is successfully 
looked up and the certificate is found to be revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_AUTH_ENABLE_CRL_CHECK_STRONG"></a><a id="ikeext_cert_auth_enable_crl_check_strong"></a><dl>
<dt><b>IKEEXT_CERT_AUTH_ENABLE_CRL_CHECK_STRONG</b></dt>
</dl>
</td>
<td width="60%">
Enable strong CRL checking. Strong checking means that a certificate will be
rejected if certificate is found to be revoked, or if any other error 
(for example, CRL could not be retrieved) takes place while performing the 
revocation checking.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_AUTH_DISABLE_SSL_CERT_VALIDATION"></a><a id="ikeext_cert_auth_disable_ssl_cert_validation"></a><dl>
<dt><b>IKEEXT_CERT_AUTH_DISABLE_SSL_CERT_VALIDATION</b></dt>
</dl>
</td>
<td width="60%">
SSL validation requires certain EKUs, like server auth EKU from a server.   This flag disables the server authentication EKU check, but still performs the other IKE-style certificate verification.

Applicable only to AuthIP.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_AUTH_ALLOW_HTTP_CERT_LOOKUP"></a><a id="ikeext_cert_auth_allow_http_cert_lookup"></a><dl>
<dt><b>IKEEXT_CERT_AUTH_ALLOW_HTTP_CERT_LOOKUP</b></dt>
</dl>
</td>
<td width="60%">
Allow lookup of peer certificate information from an HTTP URL.

Applicable only to IKEv2.

Available only on Windows 7, Windows Server 2008 R2, and later.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_AUTH_URL_CONTAINS_BUNDLE"></a><a id="ikeext_cert_auth_url_contains_bundle"></a><dl>
<dt><b>IKEEXT_CERT_AUTH_URL_CONTAINS_BUNDLE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the URL specified in the certificate authentication policy points to an encoded certificate bundle. If this flag is not specified, IKEv2 will assume that the URL points to an encoded certificate.

Applicable only to IKEv2.

Available only on Windows 7, Windows Server 2008 R2, and later.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/b137e27b-c361-4fd2-9b3b-5c2b364576d4">IKEEXT_CERT_CONFIG_TYPE</a>



<a href="https://msdn.microsoft.com/820da66b-670e-490e-bba4-c2b0afb6dfd1">IKEEXT_CERT_ROOT_CONFIG0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

