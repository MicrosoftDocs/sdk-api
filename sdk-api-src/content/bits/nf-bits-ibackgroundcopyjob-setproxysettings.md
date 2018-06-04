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

# IBackgroundCopyJob::SetProxySettings


## -description


Specifies which proxy to use to transfer files.


## -parameters




### -param ProxyUsage [in]

Specifies whether to use the user's proxy settings, not to use a proxy, or to use application-specified proxy settings. The default is to use the user's proxy settings, <b>BG_JOB_PROXY_USAGE_PRECONFIG</b>. For a list of proxy options, see the 
<a href="https://msdn.microsoft.com/e066b6c8-905f-4e18-9be7-aa3c134f9e13">BG_JOB_PROXY_USAGE</a> enumeration.


### -param ProxyList




### -param ProxyBypassList






#### - pProxyBypassList [in]

Null-terminated string that contains an optional list of host names, IP addresses, or both, that can bypass the proxy. The list is space-delimited. For details on specifying a bypass proxy, see Remarks.

This parameter must be <b>NULL</b> if the value of <i>ProxyUsage</i> is <b>BG_JOB_PROXY_USAGE_PRECONFIG</b>, <b>BG_JOB_PROXY_USAGE_NO_PROXY</b>, or <b>BG_JOB_PROXY_USAGE_AUTODETECT</b>.
						

The length of the proxy bypass list is limited to 4,000 characters, not including the null terminator.
					


#### - pProxyList [in]

Null-terminated string that contains the proxies to use to transfer files. The list is space-delimited. For details on specifying a proxy, see Remarks.

 This parameter must be <b>NULL</b> if the value of <i>ProxyUsage</i> is <b>BG_JOB_PROXY_USAGE_PRECONFIG</b>, <b>BG_JOB_PROXY_USAGE_NO_PROXY</b>, or <b>BG_JOB_PROXY_USAGE_AUTODETECT</b>.


						The length of the proxy list is limited to 4,000 characters, not including the null terminator.
					


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
<dt><b><b>S_OK</b></b></dt>
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
<a href="https://msdn.microsoft.com/e066b6c8-905f-4e18-9be7-aa3c134f9e13">BG_JOB_PROXY_USAGE</a> enumeration.

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

 If your service runs as LocalSystem, you should use the <b>SetProxySettings</b> method to explicitly specify a proxy or proxy bypass list for the account and set <i>ProxyUsage</i> to <b>BG_JOB_PROXY_USAGE_OVERRIDE</b>. For more information on using system accounts with BITS, see <a href="https://msdn.microsoft.com/43fb58d6-3a99-488f-ab43-dbb4a794fc2f">Service Accounts and BITS</a>.

BITS does not recognize the proxy settings that are set using the Proxycfg.exe file.

Specify a proxy as:

"[<i>protocol</i>=][<i>protocol</i>"://"]<i>server</i>[":"<i>port</i>]"

The valid protocols are HTTP and HTTPS. The proxy list can contain the port number that is used to access the proxy.  For example, to list an HTTP proxy, a valid string is "http=http://<i>http_proxy_name</i>:80", where <i>http_proxy_name</i> is the name of the proxy server and 80 is the port number that you must use to access the proxy. If the proxy uses the default port number for that protocol, then you can omit the port number. If a proxy name is listed by itself, you can use it as the default proxy for any protocols that do not have a specified proxy. For example, "http=http://<i>http_proxy</i><i>other_proxy</i>" uses <i>http_proxy</i> for any HTTP operations, while the HTTPS protocol uses the proxy named <i>other_proxy</i>.



You can list locally known host names or Internet Protocol (IP) addresses in the proxy bypass list. This name can contain wildcards, such as "*", that cause the application to bypass the proxy server for addresses that fit the specified pattern, for example, "*.microsoft.com" or "*.org". Wildcard characters must be the left-most characters in the name. For example, "aaa.*" is not supported. You can specify the  &lt;local&gt; macro to indicate that all local intranet sites are bypassed. Local intranet sites are considered to be all servers that do not contain a period in their name.


BITS uses the Internet Explorer proxy settings of the user if an application does not specify a proxy usage. This default behavior typically works if the application submits the job in the context of an interactive user but may not work if a service running as LocalSystem submits the job. You can specify Internet Explorer proxy settings for LocalSystem; however, it is difficult to detect these settings when problems occur.




## -see-also




<a href="https://msdn.microsoft.com/e066b6c8-905f-4e18-9be7-aa3c134f9e13">BG_JOB_PROXY_USAGE</a>



<a href="https://msdn.microsoft.com/c2d0ec9b-eaa1-4f78-9ccc-4e91d045cd94">IBackgroundCopyJob::GetProxySettings</a>
 

 

