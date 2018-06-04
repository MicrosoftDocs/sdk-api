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

# WINHTTP_CONNECTION_INFO structure


## -description


The <b>WINHTTP_CONNECTION_INFO</b> structure contains the source and destination IP address of the request that generated the response.


## -struct-fields




### -field cbSize

The size, in bytes, of the <b>WINHTTP_CONNECTION_INFO</b> structure.


### -field LocalAddress

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a> structure that contains the local IP address and port of the original request.


### -field RemoteAddress

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a> structure that contains the remote IP address and port of the original request.


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


