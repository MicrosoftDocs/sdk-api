---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.SetSecurityFlags
title: IBackgroundCopyJobHttpOptions::SetSecurityFlags (bits2_5.h)
description: Sets flags for HTTP that determine whether the certificate revocation list is checked and certain certificate errors are ignored, and the policy to use when a server redirects the HTTP request.
helpviewer_keywords: ["BG_HTTP_REDIRECT_POLICY_ALLOW_HTTPS_TO_HTTP","BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT","BG_HTTP_REDIRECT_POLICY_ALLOW_SILENT","BG_HTTP_REDIRECT_POLICY_DISALLOW","BG_HTTP_REDIRECT_POLICY_MASK","BG_SSL_ENABLE_CRL_CHECK","BG_SSL_IGNORE_CERT_CN_INVALID","BG_SSL_IGNORE_CERT_DATE_INVALID","BG_SSL_IGNORE_CERT_WRONG_USAGE","BG_SSL_IGNORE_UNKNOWN_CA","IBackgroundCopyJobHttpOptions interface [BITS]","SetSecurityFlags method","IBackgroundCopyJobHttpOptions.SetSecurityFlags","IBackgroundCopyJobHttpOptions::SetSecurityFlags","SetSecurityFlags","SetSecurityFlags method [BITS]","SetSecurityFlags method [BITS]","IBackgroundCopyJobHttpOptions interface","bits.ibackgroundcopyjobhttpoptions_setsecurityflags","bits2_5/IBackgroundCopyJobHttpOptions::SetSecurityFlags"]
old-location: bits\ibackgroundcopyjobhttpoptions_setsecurityflags.htm
tech.root: Bits
ms.assetid: afac84cb-28ab-4c80-ab39-eefe450ae3e5
ms.date: 12/05/2018
ms.keywords: BG_HTTP_REDIRECT_POLICY_ALLOW_HTTPS_TO_HTTP, BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT, BG_HTTP_REDIRECT_POLICY_ALLOW_SILENT, BG_HTTP_REDIRECT_POLICY_DISALLOW, BG_HTTP_REDIRECT_POLICY_MASK, BG_SSL_ENABLE_CRL_CHECK, BG_SSL_IGNORE_CERT_CN_INVALID, BG_SSL_IGNORE_CERT_DATE_INVALID, BG_SSL_IGNORE_CERT_WRONG_USAGE, BG_SSL_IGNORE_UNKNOWN_CA, IBackgroundCopyJobHttpOptions interface [BITS],SetSecurityFlags method, IBackgroundCopyJobHttpOptions.SetSecurityFlags, IBackgroundCopyJobHttpOptions::SetSecurityFlags, SetSecurityFlags, SetSecurityFlags method [BITS], SetSecurityFlags method [BITS],IBackgroundCopyJobHttpOptions interface, bits.ibackgroundcopyjobhttpoptions_setsecurityflags, bits2_5/IBackgroundCopyJobHttpOptions::SetSecurityFlags
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
 - IBackgroundCopyJobHttpOptions::SetSecurityFlags
 - bits2_5/IBackgroundCopyJobHttpOptions::SetSecurityFlags
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
 - IBackgroundCopyJobHttpOptions.SetSecurityFlags
---

# IBackgroundCopyJobHttpOptions::SetSecurityFlags


## -description

Sets flags for HTTP that determine whether the certificate revocation list is checked and certain certificate errors are ignored, and the policy to use when a server redirects the HTTP request.

## -parameters

### -param Flags [in]

HTTP security flags that indicate which errors to ignore when connecting to the server. You can set one or more of the following flags:

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

The following table lists some of the possible return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the headers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The flag value is not supported.

</td>
</tr>
</table>

## -remarks

If CRL checking is requested, BITS performs the check for all files in the job that specify the HTTPS protocol. The check is made for each file before the file begins transferring. If you set this value to <b>TRUE</b> after BITS has partially downloaded a file, BITS will reschedule the job and begin downloading the file again. Files that are already downloaded are not affected.

BITS uses the CRL on the local computer if the CRL is up-to-date; otherwise, BITS downloads the CRL from the certification authority (CA) that signed the certificate.

The job goes into the fatal error state if the following errors occur.

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td><b>ERROR_WINHTTP_SECURE_CERT_REV_FAILED</b></td>
<td>Unable to request CRL checking because the certificate server is offline or the CRL cannot be downloaded.</td>
</tr>
<tr>
<td><b>ERROR_WINHTTP_SECURE_CERT_REVOKED</b></td>
<td>The certificate is revoked.</td>
</tr>
</table>
 

The redirect policy applies to all files in a download job (the policy does not apply to upload jobs).

<b>Prior to BITS 3.0:  </b>The redirect policies are not supported.

If the policy is BG_HTTP_REDIRECT_POLICY_DISALLOW and the server redirects your request, the job is placed in the fatal error state with one of the following error codes. For descriptions of the error codes, see <a href="/windows/desktop/WinHttp/http-status-codes">HTTP Status Codes</a>. 

<ul>
<li>HRESULT_FROM_WIN32(HTTP_STATUS_AMBIGUOUS)</li>
<li>HRESULT_FROM_WIN32(HTTP_STATUS_MOVED)</li>
<li>HRESULT_FROM_WIN32(HTTP_STATUS_REDIRECT)</li>
<li>HRESULT_FROM_WIN32(HTTP_STATUS_REDIRECT_METHOD)</li>
<li>HRESULT_FROM_WIN32(HTTP_STATUS_REDIRECT_KEEP_VERB)</li>
</ul>
BITS does not support redirection from HTTP or HTTPs to SMB.

If peer caching is enabled and you specify BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT, the file is stored in the cache with the final redirected URL. If a peer then tries to download the file with the original URL, the peer will not find the file in the peer's cache and will end up downloading the file from the origin server.

If you specify  and the file is downloaded from the 

Note that setting BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT may affect the result when calling the <a href="/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix">IBackgroundCopyJob3::ReplaceRemotePrefix</a> method. If a server redirected your request, BITS will have already changed the original URL to the final redirected URL, so calling the <b>ReplaceRemotePrefix</b> method will not find files with the original URL.

## -see-also

<a href="/windows/desktop/api/bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions">IBackgroundCopyJobHttpOptions</a>



<a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-getsecurityflags">IBackgroundCopyJobHttpOptions::GetSecurityFlags</a>