---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.GetSecurityFlags
title: IBackgroundCopyJobHttpOptions::GetSecurityFlags (bits2_5.h)
description: Retrieves the flags for HTTP that determine whether the certificate revocation list is checked and certain certificate errors are ignored, and the policy to use when a server redirects the HTTP request.
helpviewer_keywords: ["BG_HTTP_REDIRECT_POLICY_ALLOW_HTTPS_TO_HTTP","BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT","BG_HTTP_REDIRECT_POLICY_ALLOW_SILENT","BG_HTTP_REDIRECT_POLICY_DISALLOW","BG_HTTP_REDIRECT_POLICY_MASK","BG_SSL_ENABLE_CRL_CHECK","BG_SSL_IGNORE_CERT_CN_INVALID","BG_SSL_IGNORE_CERT_DATE_INVALID","BG_SSL_IGNORE_CERT_WRONG_USAGE","BG_SSL_IGNORE_UNKNOWN_CA","GetSecurityFlags","GetSecurityFlags method [BITS]","GetSecurityFlags method [BITS]","IBackgroundCopyJobHttpOptions interface","IBackgroundCopyJobHttpOptions interface [BITS]","GetSecurityFlags method","IBackgroundCopyJobHttpOptions.GetSecurityFlags","IBackgroundCopyJobHttpOptions::GetSecurityFlags","bits.ibackgroundcopyjobhttpoptions_getsecurityflags","bits2_5/IBackgroundCopyJobHttpOptions::GetSecurityFlags"]
old-location: bits\ibackgroundcopyjobhttpoptions_getsecurityflags.htm
tech.root: Bits
ms.assetid: 75104dca-086e-45f6-ad9e-a96730b37433
ms.date: 12/05/2018
ms.keywords: BG_HTTP_REDIRECT_POLICY_ALLOW_HTTPS_TO_HTTP, BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT, BG_HTTP_REDIRECT_POLICY_ALLOW_SILENT, BG_HTTP_REDIRECT_POLICY_DISALLOW, BG_HTTP_REDIRECT_POLICY_MASK, BG_SSL_ENABLE_CRL_CHECK, BG_SSL_IGNORE_CERT_CN_INVALID, BG_SSL_IGNORE_CERT_DATE_INVALID, BG_SSL_IGNORE_CERT_WRONG_USAGE, BG_SSL_IGNORE_UNKNOWN_CA, GetSecurityFlags, GetSecurityFlags method [BITS], GetSecurityFlags method [BITS],IBackgroundCopyJobHttpOptions interface, IBackgroundCopyJobHttpOptions interface [BITS],GetSecurityFlags method, IBackgroundCopyJobHttpOptions.GetSecurityFlags, IBackgroundCopyJobHttpOptions::GetSecurityFlags, bits.ibackgroundcopyjobhttpoptions_getsecurityflags, bits2_5/IBackgroundCopyJobHttpOptions::GetSecurityFlags
req.header: bits2_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJobHttpOptions::GetSecurityFlags
 - bits2_5/IBackgroundCopyJobHttpOptions::GetSecurityFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJobHttpOptions.GetSecurityFlags
---

# IBackgroundCopyJobHttpOptions::GetSecurityFlags


## -description

Retrieves the flags for HTTP that determine whether the certificate revocation list is checked and certain certificate errors are ignored, and the policy to use when a server redirects the HTTP request.

## -parameters

### -param pFlags [out]

HTTP security flags that indicate which errors to ignore when connecting to the server. One or more of the following flags can be set:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_SSL_ENABLE_CRL_CHECK"></a><a id="bg_ssl_enable_crl_check"></a><dl>
<dt><b>BG_SSL_ENABLE_CRL_CHECK</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Check the certificate revocation list (CRL) to verify that the server certificate has not been revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_SSL_IGNORE_CERT_CN_INVALID"></a><a id="bg_ssl_ignore_cert_cn_invalid"></a><dl>
<dt><b>BG_SSL_IGNORE_CERT_CN_INVALID</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Ignores errors caused when the certificate host name of the server does not match the host name in the request.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_SSL_IGNORE_CERT_DATE_INVALID"></a><a id="bg_ssl_ignore_cert_date_invalid"></a><dl>
<dt><b>BG_SSL_IGNORE_CERT_DATE_INVALID</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Ignores errors caused by an expired certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_SSL_IGNORE_UNKNOWN_CA"></a><a id="bg_ssl_ignore_unknown_ca"></a><dl>
<dt><b>BG_SSL_IGNORE_UNKNOWN_CA</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Ignore errors associated with an unknown  certification authority (CA).

</td>
</tr>
<tr>
<td width="40%"><a id="BG_SSL_IGNORE_CERT_WRONG_USAGE"></a><a id="bg_ssl_ignore_cert_wrong_usage"></a><dl>
<dt><b>BG_SSL_IGNORE_CERT_WRONG_USAGE</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Ignore errors associated with the use of a certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_HTTP_REDIRECT_POLICY_ALLOW_SILENT"></a><a id="bg_http_redirect_policy_allow_silent"></a><dl>
<dt><b>BG_HTTP_REDIRECT_POLICY_ALLOW_SILENT</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Allows the server to redirect your request to another server. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT"></a><a id="bg_http_redirect_policy_allow_report"></a><dl>
<dt><b>BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Allows the server to redirect your request to another server. BITS updates the remote name with the final URL.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_HTTP_REDIRECT_POLICY_DISALLOW"></a><a id="bg_http_redirect_policy_disallow"></a><dl>
<dt><b>BG_HTTP_REDIRECT_POLICY_DISALLOW</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Places the job in the fatal error state when the server redirects your request to another server. BITS updates the remote name with the redirected URL.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_HTTP_REDIRECT_POLICY_MASK"></a><a id="bg_http_redirect_policy_mask"></a><dl>
<dt><b>BG_HTTP_REDIRECT_POLICY_MASK</b></dt>
<dt>0x0700</dt>
</dl>
</td>
<td width="60%">
Bitmask that you can use with the security flag value to determine which redirect policy is in effect. It does not include the flag ALLOW_HTTPS_TO_HTTP.

The following example shows how to use this mask to test for the BG_HTTP_REDIRECT_POLICY_DISALLOW redirection policy.

<code>if (BG_HTTP_REDIRECT_POLICY_DISALLOW == (flags &amp; BG_HTTP_REDIRECT_POLICY_MASK))</code>

</td>
</tr>
<tr>
<td width="40%"><a id="BG_HTTP_REDIRECT_POLICY_ALLOW_HTTPS_TO_HTTP"></a><a id="bg_http_redirect_policy_allow_https_to_http"></a><dl>
<dt><b>BG_HTTP_REDIRECT_POLICY_ALLOW_HTTPS_TO_HTTP</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Allows the server to redirect an HTTPS request to an HTTP URL.

You can combine this flag with BG_HTTP_REDIRECT_POLICY_ALLOW_SILENT and BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT. 

</td>
</tr>
</table>

## -returns

Returns S_OK when successful.

## -see-also

<a href="/windows/desktop/api/bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions">IBackgroundCopyJobHttpOptions</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">IBackgroundCopyJobHttpOptions::SetSecurityFlags</a>