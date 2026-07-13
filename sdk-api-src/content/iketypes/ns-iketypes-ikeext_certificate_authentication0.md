---
UID: NS:iketypes.IKEEXT_CERTIFICATE_AUTHENTICATION0_
title: IKEEXT_CERTIFICATE_AUTHENTICATION0 (iketypes.h)
description: Is used to specify various parameters for authentication with certificates. (IKEEXT_CERTIFICATE_AUTHENTICATION0)
helpviewer_keywords: ["IKEEXT_CERTIFICATE_AUTHENTICATION0","IKEEXT_CERTIFICATE_AUTHENTICATION0 structure [Filtering]","IKEEXT_CERT_AUTH_ALLOW_HTTP_CERT_LOOKUP","IKEEXT_CERT_AUTH_DISABLE_SSL_CERT_VALIDATION","IKEEXT_CERT_AUTH_ENABLE_CRL_CHECK_STRONG","IKEEXT_CERT_AUTH_FLAG_DISABLE_CRL_CHECK","IKEEXT_CERT_AUTH_FLAG_SSL_ONE_WAY","IKEEXT_CERT_AUTH_URL_CONTAINS_BUNDLE","fwp.ikeext_certificate_authentication0","iketypes/IKEEXT_CERTIFICATE_AUTHENTICATION0"]
old-location: fwp\ikeext_certificate_authentication0.htm
tech.root: fwp
ms.assetid: e9f9625d-b68b-4b7d-a587-39dac04dd991
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERTIFICATE_AUTHENTICATION0, IKEEXT_CERTIFICATE_AUTHENTICATION0 structure [Filtering], IKEEXT_CERT_AUTH_ALLOW_HTTP_CERT_LOOKUP, IKEEXT_CERT_AUTH_DISABLE_SSL_CERT_VALIDATION, IKEEXT_CERT_AUTH_ENABLE_CRL_CHECK_STRONG, IKEEXT_CERT_AUTH_FLAG_DISABLE_CRL_CHECK, IKEEXT_CERT_AUTH_FLAG_SSL_ONE_WAY, IKEEXT_CERT_AUTH_URL_CONTAINS_BUNDLE, fwp.ikeext_certificate_authentication0, iketypes/IKEEXT_CERTIFICATE_AUTHENTICATION0
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_CERTIFICATE_AUTHENTICATION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CERTIFICATE_AUTHENTICATION0_
 - iketypes/IKEEXT_CERTIFICATE_AUTHENTICATION0_
 - IKEEXT_CERTIFICATE_AUTHENTICATION0
 - iketypes/IKEEXT_CERTIFICATE_AUTHENTICATION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_CERTIFICATE_AUTHENTICATION0
---

# IKEEXT_CERTIFICATE_AUTHENTICATION0 structure


## -description

The [IKEEXT_CERTIFICATE_AUTHENTICATION1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_certificate_authentication1) is available. For Windows 8, [IKEEXT_CERTIFICATE_AUTHENTICATION2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_certificate_authentication2) is available.</div>
<div> </div>

## -struct-fields

### -field inboundConfigType

Certificate configuration type for inbound peer certificate verification.

See [IKEEXT_CERT_CONFIG_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_cert_config_type) for more information.

### -field inboundRootArraySize

Number of elements in the <b>inboundRootArray</b> member.

Available when <b>inboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST</b>.

### -field inboundRootArray

Explicit trust list for verifying the peer certificate chain.

Available when <b>inboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST</b>.

See [IKEEXT_CERT_ROOT_CONFIG0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_root_config0) for more information.

### -field inboundEnterpriseStoreConfig

Enterprise store configuration for verifying the peer certificate chain.

Available when <b>inboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_ENTERPRISE_STORE</b>.

See [IKEEXT_CERT_ROOT_CONFIG0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_root_config0) for more information.

### -field inboundTrustedRootStoreConfig

Trusted root store configuration for verifying the peer certificate chain.

Available when <b>inboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE</b>.

See [IKEEXT_CERT_ROOT_CONFIG0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_root_config0) for more information.

### -field outboundConfigType

Certificate configuration type for outbound local certificate verification.

See [IKEEXT_CERT_CONFIG_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_cert_config_type) for more information.

### -field outboundRootArraySize

Number of elements in the <b>outboundRootArray</b> member.

Available when <b>outboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST</b>.

### -field outboundRootArray

Explicit trust list for selecting a certificate chain to send to the peer.

Available when <b>outboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST</b>.

See [IKEEXT_CERT_ROOT_CONFIG0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_root_config0) for more information.

### -field outboundEnterpriseStoreConfig

Enterprise store configuration for selecting  the certificate chain.

Available when <b>outboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_ENTERPRISE_STORE</b>.

See [IKEEXT_CERT_ROOT_CONFIG0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_root_config0) for more information.

### -field outboundTrustedRootStoreConfig

Trusted root store configuration for selecting the certificate chain.

Available when <b>outboundConfigType</b> is <b>IKEEXT_CERT_CONFIG_ROOT_STORE</b>.

See [IKEEXT_CERT_ROOT_CONFIG0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_root_config0) for more information.

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

[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



[IKEEXT_CERT_CONFIG_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_cert_config_type)



[IKEEXT_CERT_ROOT_CONFIG0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_root_config0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
