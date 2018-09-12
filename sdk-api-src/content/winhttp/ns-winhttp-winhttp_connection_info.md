---
UID: NS:winhttp.WINHTTP_CONNECTION_INFO
title: WINHTTP_CONNECTION_INFO
author: windows-sdk-content
description: The WINHTTP_CONNECTION_INFO structure contains the source and destination IP address of the request that generated the response.
old-location: http\winhttp_connection_info.htm
tech.root: WinHttp
ms.assetid: cb6e10f8-a480-41ac-b4d3-f09cfc663780
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WINHTTP_CONNECTION_INFO, WINHTTP_CONNECTION_INFO structure [HTTP], http.winhttp_connection_info, winhttp/WINHTTP_CONNECTION_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winhttp.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_CONNECTION_INFO
product: Windows
targetos: Windows
req.typenames: WINHTTP_CONNECTION_INFO
req.redist: 
---

# WINHTTP_CONNECTION_INFO structure


## -description


The <b>WINHTTP_CONNECTION_INFO</b> structure contains the source and destination IP address of the request that generated the response.


## -struct-fields




### -field cbSize

The size, in bytes, of the <b>WINHTTP_CONNECTION_INFO</b> structure.


### -field LocalAddress

A <a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a> structure that contains the local IP address and port of the original request.


### -field RemoteAddress

A <a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a> structure that contains the remote IP address and port of the original request.


## -remarks



When <a href="https://msdn.microsoft.com/0b79e73b-9f6a-42eb-9108-1ba142ad7c48">WinHttpReceiveResponse</a> returns, the application can retrieve the source and destination IP address of the request that generated the response. The application calls <a href="https://msdn.microsoft.com/47973eab-de70-47bf-9713-97b87a500cfa">WinHttpQueryOption</a> with the <b>WINHTTP_OPTION_CONNECTION_INFO</b> option, and provides the <b>WINHTTP_CONNECTION_INFO</b> structure in the <i>lpBuffer</i> parameter.


#### Examples

The following code example shows the call to <a href="https://msdn.microsoft.com/47973eab-de70-47bf-9713-97b87a500cfa">WinHttpQueryOption</a>. Winsock2.h must be included before Winhttp.h when using the <b>WINHTTP_OPTION_CONNECTION_INFO</b> option.

If the original request was redirected, the <b>WINHTTP_CONNECTION_INFO</b> structure contains the IP address and port of the request that resulted from the first non-30X response.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WINHTTP_CONNECTION_INFO ConnInfo;
DWORD dwConnInfoSize = sizeof(WINHTTP_CONNECTION_INFO);

WinHttpQueryOption( hRequest,
                    WINHTTP_OPTION_CONNECTION_INFO,
                    &amp;ConnInfo,
                    &amp;dwConnInfoSize);
</pre>
</td>
</tr>
</table></span></div>


