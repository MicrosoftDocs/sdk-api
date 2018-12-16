---
UID: NS:mstcpip._SOCKET_SECURITY_QUERY_INFO
title: SOCKET_SECURITY_QUERY_INFO
author: windows-sdk-content
description: Contains security information returned by the WSAQuerySocketSecurity function.
old-location: winsock\socket_security_query_info.htm
tech.root: winsock
ms.assetid: 90439ff6-e6a8-4124-b280-a65b9ca12787
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SOCKET_INFO_CONNECTION_ENCRYPTED, SOCKET_INFO_CONNECTION_SECURED, SOCKET_SECURITY_QUERY_INFO, SOCKET_SECURITY_QUERY_INFO structure [Winsock], mstcpip/SOCKET_SECURITY_QUERY_INFO, winsock.socket_security_query_info
ms.topic: struct
req.header: mstcpip.h
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
 - Mstcpip.h
api_name:
 - SOCKET_SECURITY_QUERY_INFO
product: Windows
targetos: Windows
req.typenames: SOCKET_SECURITY_QUERY_INFO
req.redist: 
---

# SOCKET_SECURITY_QUERY_INFO structure


## -description


The <b>SOCKET_SECURITY_QUERY_INFO</b> structure contains security information returned by the <a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a> function.


## -struct-fields




### -field SecurityProtocol

A <a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a> value that identifies the protocol used to secure the traffic.


### -field Flags

The  set of possible security flags for the connection defined in the <i>Mstcpip.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SOCKET_INFO_CONNECTION_SECURED"></a><a id="socket_info_connection_secured"></a><dl>
<dt><b>SOCKET_INFO_CONNECTION_SECURED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If present, traffic is being secured by a security protocol.  If absent, the traffic is flowing in the clear.

</td>
</tr>
<tr>
<td width="40%"><a id="SOCKET_INFO_CONNECTION_ENCRYPTED"></a><a id="socket_info_connection_encrypted"></a><dl>
<dt><b>SOCKET_INFO_CONNECTION_ENCRYPTED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If present, the connection traffic is being encrypted.  The          <b>SOCKET_INFO_CONNECTION_SECURED</b> flag is always set when this flag is present.

</td>
</tr>
</table>
 


### -field PeerApplicationAccessTokenHandle

A handle to the access token that represents the account under which the peer application is running.  After using the token for access checks, the application should close the handle using the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


### -field PeerMachineAccessTokenHandle

A handle to the access token for the peer computer's account during the course of the application.  After using the token for access checks, the application should close the handle using the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


## -remarks



The <b>SOCKET_SECURITY_QUERY_INFO</b> structure  is supported on Windows Vistaand later.

The <b>SOCKET_SECURITY_QUERY_INFO</b> structure  is used by the <a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a> function to return information about the security applied to a connection on a socket.




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

