---
UID: NS:wininet.INTERNET_DIAGNOSTIC_SOCKET_INFO
title: INTERNET_DIAGNOSTIC_SOCKET_INFO
author: windows-sdk-content
description: The INTERNET_DIAGNOSTIC_SOCKET_INFO structure is returned by the InternetQueryOption function when the INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO flag is passed to it together with a handle to an HTTP Request.
old-location: wininet\internet_diagnostic_socket_info.htm
old-project: WinInet
ms.assetid: a659fcfd-49c4-4d2b-8b1d-62deb033bf8d
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "* LPINTERNET_DIAGNOSTIC_SOCKET_INFO, * LPINTERNET_DIAGNOSTIC_SOCKET_INFO structure [WinINet], *LPINTERNET_DIAGNOSTIC_SOCKET_INFO, IDSI_FLAG_KEEP_ALIVE, IDSI_FLAG_PROXY, IDSI_FLAG_SECURE, IDSI_FLAG_TUNNEL, INTERNET_DIAGNOSTIC_SOCKET_INFO, INTERNET_DIAGNOSTIC_SOCKET_INFO structure [WinINet], wininet.internet_diagnostic_socket_info, wininet/* LPINTERNET_DIAGNOSTIC_SOCKET_INFO, wininet/INTERNET_DIAGNOSTIC_SOCKET_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wininet.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: INTERNET_DIAGNOSTIC_SOCKET_INFO, *LPINTERNET_DIAGNOSTIC_SOCKET_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_DIAGNOSTIC_SOCKET_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# INTERNET_DIAGNOSTIC_SOCKET_INFO structure


## -description


The <b>INTERNET_DIAGNOSTIC_SOCKET_INFO</b> structure is returned by the <a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a> function when the INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO flag is passed to it together with a handle to an HTTP Request. The <b>INTERNET_DIAGNOSTIC_SOCKET_INFO</b> structure contains information about the socket associated with that HTTP Request.


## -struct-fields




### -field Socket

Descriptor that identifies the socket associated with the specified HTTP Request.


### -field SourcePort

The address of the port at which the HTTP Request and response was received.


### -field DestPort

The address of the port at which the response was sent.


### -field Flags

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDSI_FLAG_KEEP_ALIVE"></a><a id="idsi_flag_keep_alive"></a><dl>
<dt><b>IDSI_FLAG_KEEP_ALIVE</b></dt>
</dl>
</td>
<td width="60%">
	Set if the connection is from the "keep-alive" pool.

</td>
</tr>
<tr>
<td width="40%"><a id="IDSI_FLAG_SECURE"></a><a id="idsi_flag_secure"></a><dl>
<dt><b>IDSI_FLAG_SECURE</b></dt>
</dl>
</td>
<td width="60%">
Set if the HTTP Request is using a secure socket.

</td>
</tr>
<tr>
<td width="40%"><a id="IDSI_FLAG_PROXY"></a><a id="idsi_flag_proxy"></a><dl>
<dt><b>IDSI_FLAG_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Set if a proxy is being used to reach the server.

</td>
</tr>
<tr>
<td width="40%"><a id="IDSI_FLAG_TUNNEL"></a><a id="idsi_flag_tunnel"></a><dl>
<dt><b>IDSI_FLAG_TUNNEL</b></dt>
</dl>
</td>
<td width="60%">
Set if a proxy is being used to create a tunnel.

</td>
</tr>
</table>
 


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a>
 

 

