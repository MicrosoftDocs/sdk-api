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

# WINHTTP_PROXY_INFO structure


## -description


The <b>WINHTTP_PROXY_INFO</b> structure contains the session or default proxy configuration.


## -struct-fields




### -field dwAccessType

Unsigned long integer value that contains the access type. This can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_NO_PROXY"></a><a id="winhttp_access_type_no_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_NO_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Internet accessed through a direct connection. 

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_DEFAULT_PROXY"></a><a id="winhttp_access_type_default_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Applies only when setting proxy information. 

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_NAMED_PROXY"></a><a id="winhttp_access_type_named_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Internet accessed using a proxy. 

</td>
</tr>
</table>
 


### -field lpszProxy

Pointer to a string value that contains the proxy server list.


### -field lpszProxyBypass

Pointer to a string value that contains the proxy bypass list.


## -remarks



This structure is used with 
<a href="https://msdn.microsoft.com/bcf1da09-5787-4d2a-82ae-6965e27fa477">WinHttpSetOption</a> and 
<a href="https://msdn.microsoft.com/47973eab-de70-47bf-9713-97b87a500cfa">WinHttpQueryOption</a> to get or set the proxy configuration for the current session by specifying the WINHTTP_OPTION_PROXY flag.

This structure is used with 
<a href="https://msdn.microsoft.com/df95703b-8fa0-4ea4-b9e6-7f19aa8c1941">WinHttpSetDefaultProxyConfiguration</a> and 
<a href="https://msdn.microsoft.com/e8038b4b-b9d0-481a-a49c-26201d72bc7a">WinHttpGetDefaultProxyConfiguration</a> to get or set the default proxy configuration in the registry.

The proxy server list contains one or more of the following strings separated by semicolons or whitespace.


<pre class="syntax" xml:space="preserve"><code>([&lt;scheme&gt;=][&lt;scheme&gt;"://"]&lt;server&gt;[":"&lt;port&gt;])
</code></pre>
The proxy bypass list contains one or more server names separated by semicolons or whitespace.  The proxy bypass list can also contain the string "&lt;local&gt;" to indicate that all local intranet sites are bypassed.  Local intranet sites are considered to be all servers that do not contain a period in their name.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP
		  Versions</a>
 

 

