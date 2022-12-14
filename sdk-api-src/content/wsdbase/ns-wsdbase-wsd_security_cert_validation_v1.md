---
UID: NS:wsdbase._WSD_SECURITY_CERT_VALIDATION_V1
title: WSD_SECURITY_CERT_VALIDATION_V1 (wsdbase.h)
description: Represents the criteria for matching client certificates against those of an HTTPS server.W
helpviewer_keywords: ["*PWSD_SECURITY_CERT_VALIDATION","WSDAPI_SSL_CERT_DEFAULT_CHECKS","WSDAPI_SSL_CERT_IGNORE_EXPIRY","WSDAPI_SSL_CERT_IGNORE_INVALID_CN","WSDAPI_SSL_CERT_IGNORE_REVOCATION","WSDAPI_SSL_CERT_IGNORE_UNKNOWN_CA","WSDAPI_SSL_CERT_IGNORE_WRONG_USAGE","WSD_SECURITY_CERT_VALIDATION","WSD_SECURITY_CERT_VALIDATION structure","WSD_SECURITY_CERT_VALIDATION_V1","_WSD_SECURITY_CERT_VALIDATION","ncd.wsd_security_cert_validation","wsdbase/WSD_SECURITY_CERT_VALIDATION"]
old-location: ncd\wsd_security_cert_validation.htm
tech.root: ncd
ms.assetid: 1bc157c2-f3c2-4b67-a6ae-251ba1cb0379
ms.date: 12/05/2018
ms.keywords: '*PWSD_SECURITY_CERT_VALIDATION, WSDAPI_SSL_CERT_DEFAULT_CHECKS, WSDAPI_SSL_CERT_IGNORE_EXPIRY, WSDAPI_SSL_CERT_IGNORE_INVALID_CN, WSDAPI_SSL_CERT_IGNORE_REVOCATION, WSDAPI_SSL_CERT_IGNORE_UNKNOWN_CA, WSDAPI_SSL_CERT_IGNORE_WRONG_USAGE, WSD_SECURITY_CERT_VALIDATION, WSD_SECURITY_CERT_VALIDATION structure, WSD_SECURITY_CERT_VALIDATION_V1, _WSD_SECURITY_CERT_VALIDATION, ncd.wsd_security_cert_validation, wsdbase/WSD_SECURITY_CERT_VALIDATION'
req.header: wsdbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WSD_SECURITY_CERT_VALIDATION_V1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SECURITY_CERT_VALIDATION_V1
 - wsdbase/_WSD_SECURITY_CERT_VALIDATION_V1
 - WSD_SECURITY_CERT_VALIDATION_V1
 - wsdbase/WSD_SECURITY_CERT_VALIDATION_V1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wsdbase.h
api_name:
 - WSD_SECURITY_CERT_VALIDATION
---

# WSD_SECURITY_CERT_VALIDATION_V1 structure


## -description

Represents the criteria for matching client certificates against those of an HTTPS server.

Do not use <a href="/previous-versions/windows/desktop/legacy/hh437346(v=vs.85)">WSD_SECURITY_CERT_VALIDATION_V1</a> directly in your code; using <b>WSD_SECURITY_CERT_VALIDATION</b> instead ensures that the proper version, based on the Windows version.

## -struct-fields

### -field certMatchArray

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structures that contain certificates to be matched against those provided by the HTTPS server or client.  Only one matching certificate is required for validation.  This parameter can be NULL.

### -field dwCertMatchArrayCount

The count of certificates in <i>certMatchArray</i>.

### -field hCertMatchStore

A handle to a certificate store that contains certificates to be matched against those provided by the HTTPS server or client.  Only one matching certificate is required for validation.  This parameter can be NULL.

### -field hCertIssuerStore

A handle to a certificate store that contains root certificates against which a certificate from the HTTPS server or client should chain to.  Validation succeeds as long as the certificate chains up to at least one root certificate.  This parameter can be NULL.

### -field dwCertCheckOptions

A bitwise OR combination of values that specify which certificate checks to ignore.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_SSL_CERT_DEFAULT_CHECKS"></a><a id="wsdapi_ssl_cert_default_checks"></a><dl>
<dt><b>WSDAPI_SSL_CERT_DEFAULT_CHECKS</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Handle any revoked certificate errors.

</td>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_SSL_CERT_IGNORE_REVOCATION"></a><a id="wsdapi_ssl_cert_ignore_revocation"></a><dl>
<dt><b>WSDAPI_SSL_CERT_IGNORE_REVOCATION</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Ignore revoked certificate errors.

</td>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_SSL_CERT_IGNORE_EXPIRY"></a><a id="wsdapi_ssl_cert_ignore_expiry"></a><dl>
<dt><b>WSDAPI_SSL_CERT_IGNORE_EXPIRY</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Ignore expired certificate errors.

</td>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_SSL_CERT_IGNORE_WRONG_USAGE"></a><a id="wsdapi_ssl_cert_ignore_wrong_usage"></a><dl>
<dt><b>WSDAPI_SSL_CERT_IGNORE_WRONG_USAGE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Ignore certificate use errors.

</td>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_SSL_CERT_IGNORE_UNKNOWN_CA"></a><a id="wsdapi_ssl_cert_ignore_unknown_ca"></a><dl>
<dt><b>WSDAPI_SSL_CERT_IGNORE_UNKNOWN_CA</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Ignore unknown certificate authority errors.

</td>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_SSL_CERT_IGNORE_INVALID_CN"></a><a id="wsdapi_ssl_cert_ignore_invalid_cn"></a><dl>
<dt><b>WSDAPI_SSL_CERT_IGNORE_INVALID_CN</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Ignore invalid common name certificate errors.

</td>
</tr>
</table>

## -remarks

This structure is used in the <b>pConfigData</b> member of the <a href="/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_param">WSD_CONFIG_PARAM</a> structure. 

When the <b>configParamType</b> of <a href="/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_param">WSD_CONFIG_PARAM</a> is <b>WSD_SECURITY_SSL_SERVER_CERT_VALIDATION</b>, this structure can be used to validate SSL server certificates presented by an SSL server.



When the <b>configParamType</b> of <a href="/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_param">WSD_CONFIG_PARAM</a> is <b>WSD_SECURITY_SSL_CLIENT_CERT_VALIDATION</b>, this structure can be used to validate SSL client certificates presented by an SSL client.

<b>WSD_SECURITY_CERT_VALIDATION</b> defines 3 certificate matching mechanisms.  To obtain a match, at least one such mechanism must be satisfied.

If the application is built using Windows 8 SDK targeted for Windows 8 OS, <b>WSD_SECURITY_CERT_VALIDATION</b> resolves into the new structure. However, as a result, the application can then only run on Windows 8 machines.

If the application is built using Windows 8 SDK targeted for Windows 7 OS, <b>WSD_SECURITY_CERT_VALIDATION</b> will resolve into the old structure (<a href="/previous-versions/windows/desktop/legacy/hh437346(v=vs.85)">WSD_SECURITY_CERT_VALIDATION_V1</a>). While it's a given that the application will be supported for Windows 7, it also  on Windows 8 since <b>wsdapi.dll</b> on Windows 8 will handle both the old and the newer versions of this structure.

An application already built using Windows 7 SDK will use the old version of this structure. It will run fine on Windows 8 since <b>wsdapi.dll</b> on Windows 8 can handle both versions.
