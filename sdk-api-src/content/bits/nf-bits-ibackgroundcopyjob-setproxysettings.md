---
UID: NF:bits.IBackgroundCopyJob.SetProxySettings
title: IBackgroundCopyJob::SetProxySettings (bits.h)
description: Specifies which proxy to use to transfer files.
helpviewer_keywords: ["IBackgroundCopyJob interface [BITS]","SetProxySettings method","IBackgroundCopyJob.SetProxySettings","IBackgroundCopyJob::SetProxySettings","SetProxySettings","SetProxySettings method [BITS]","SetProxySettings method [BITS]","IBackgroundCopyJob interface","_drz_ibackgroundcopyjob_setproxysettings","bits.ibackgroundcopyjob_setproxysettings","bits/IBackgroundCopyJob::SetProxySettings"]
old-location: bits\ibackgroundcopyjob_setproxysettings.htm
tech.root: Bits
ms.assetid: fd21a17b-1049-4dd9-a08b-da84699b8006
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob interface [BITS],SetProxySettings method, IBackgroundCopyJob.SetProxySettings, IBackgroundCopyJob::SetProxySettings, SetProxySettings, SetProxySettings method [BITS], SetProxySettings method [BITS],IBackgroundCopyJob interface, _drz_ibackgroundcopyjob_setproxysettings, bits.ibackgroundcopyjob_setproxysettings, bits/IBackgroundCopyJob::SetProxySettings
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob::SetProxySettings
 - bits/IBackgroundCopyJob::SetProxySettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.SetProxySettings
---

# IBackgroundCopyJob::SetProxySettings


## -description

Specifies which proxy to use to transfer files.

## -parameters

### -param ProxyUsage [in]

Specifies whether to use the user's proxy settings, not to use a proxy, or to use application-specified proxy settings. The default is to use the user's proxy settings, <b>BG_JOB_PROXY_USAGE_PRECONFIG</b>. For a list of proxy options, see the 
<a href="/windows/desktop/api/bits/ne-bits-bg_job_proxy_usage">BG_JOB_PROXY_USAGE</a> enumeration.

### -param ProxyList [in]

Null-terminated string that contains the proxies to use to transfer files. The list is space-delimited. For details on specifying a proxy, see Remarks.

 This parameter must be <b>NULL</b> if the value of <i>ProxyUsage</i> is <b>BG_JOB_PROXY_USAGE_PRECONFIG</b>, <b>BG_JOB_PROXY_USAGE_NO_PROXY</b>, or <b>BG_JOB_PROXY_USAGE_AUTODETECT</b>.

The length of the proxy list is limited to 4,000 characters, not including the null terminator.

### -param ProxyBypassList [in]

Null-terminated string that contains an optional list of host names, IP addresses, or both, that can bypass the proxy. The list is space-delimited. For details on specifying a bypass proxy, see Remarks.

This parameter must be <b>NULL</b> if the value of <i>ProxyUsage</i> is <b>BG_JOB_PROXY_USAGE_PRECONFIG</b>, <b>BG_JOB_PROXY_USAGE_NO_PROXY</b>, or <b>BG_JOB_PROXY_USAGE_AUTODETECT</b>.
						

The length of the proxy bypass list is limited to 4,000 characters, not including the null terminator.

## -returns

This method returns the following <b>HRESULT</b> values, as well as others.

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
Proxy was successfully specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The value for <i>ProxyUsage</i> is not defined in the 
<a href="/windows/desktop/api/bits/ne-bits-bg_job_proxy_usage">BG_JOB_PROXY_USAGE</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_PROXY_LIST_TOO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>pProxyList</i> buffer cannot exceed 32 KB.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_PROXY_BYPASS_LIST_TOO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>pProxyBypassList</i> cannot exceed 32 KB.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be <b>BG_JOB_STATE_CANCELLED</b> or <b>BG_JOB_STATE_ACKNOWLEDGED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pProxyList</i> parameter cannot be <b>NULL</b> if <i>ProxyUsage</i> is <b>BG_JOB_PROXY_USAGE_OVERRIDE</b>.

</td>
</tr>
</table>

## -remarks

The proxy information you provide is validated at run time. If the proxy information is invalid, the job enters the <b>BG_JOB_STATE_ERROR</b> state with a <b>BG_E_INVALID_PROXY_INFO</b> error code.

 If your service runs as LocalSystem, you should use the <b>SetProxySettings</b> method to explicitly specify a proxy or proxy bypass list for the account and set <i>ProxyUsage</i> to <b>BG_JOB_PROXY_USAGE_OVERRIDE</b>. For more information on using system accounts with BITS, see <a href="/windows/desktop/Bits/service-accounts-and-bits">Service Accounts and BITS</a>.

BITS does not recognize the proxy settings that are set using the Proxycfg.exe file.

Specify a proxy as:

"[<i>protocol</i>=][<i>protocol</i>"://"]<i>server</i>[":"<i>port</i>]"

The valid protocols are HTTP and HTTPS. The proxy list can contain the port number that is used to access the proxy.  For example, to list an HTTP proxy, a valid string is "http=http://<i>http_proxy_name</i>:80", where <i>http_proxy_name</i> is the name of the proxy server and 80 is the port number that you must use to access the proxy. If the proxy uses the default port number for that protocol, then you can omit the port number. If a proxy name is listed by itself, you can use it as the default proxy for any protocols that do not have a specified proxy. For example, "http=http://<i>http_proxy</i><i>other_proxy</i>" uses <i>http_proxy</i> for any HTTP operations, while the HTTPS protocol uses the proxy named <i>other_proxy</i>.



You can list locally known host names or Internet Protocol (IP) addresses in the proxy bypass list. This name can contain wildcards, such as "*", that cause the application to bypass the proxy server for addresses that fit the specified pattern, for example, "*.microsoft.com" or "*.org". Wildcard characters must be the left-most characters in the name. For example, "aaa.*" is not supported. You can specify the  &lt;local&gt; macro to indicate that all local intranet sites are bypassed. Local intranet sites are considered to be all servers that do not contain a period in their name.


BITS uses the Internet Explorer proxy settings of the user if an application does not specify a proxy usage. This default behavior typically works if the application submits the job in the context of an interactive user but may not work if a service running as LocalSystem submits the job. You can specify Internet Explorer proxy settings for LocalSystem; however, it is difficult to detect these settings when problems occur.

## -see-also

<a href="/windows/desktop/api/bits/ne-bits-bg_job_proxy_usage">BG_JOB_PROXY_USAGE</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getproxysettings">IBackgroundCopyJob::GetProxySettings</a>