---
UID: NF:wsdbase.IWSDUdpAddress.SetSockaddr
title: IWSDUdpAddress::SetSockaddr
author: windows-sdk-content
description: Sets the socket address information.
old-location: ncd\iwsdudpaddress_setsockaddr.htm
tech.root: WsdApi
ms.assetid: a8c6cc53-bba6-44ef-8c1e-f357e11793b4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWSDUdpAddress interface,SetSockaddr method, IWSDUdpAddress.SetSockaddr, IWSDUdpAddress::SetSockaddr, SetSockaddr, SetSockaddr method, SetSockaddr method,IWSDUdpAddress interface, ncd.iwsdudpaddress_setsockaddr, wsdbase/IWSDUdpAddress::SetSockaddr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDUdpAddress.SetSockaddr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wsdbase.h
: 
- IWSDUdpAddress.SetSockaddr
: 
---

# IWSDUdpAddress::SetSockaddr


## -description


Sets the socket address information.


## -parameters




### -param pSockAddr [in]

Pointer to a <a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a> structure.


## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pSockAddr</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(WSAEINVAL)</b></dt>
</dl>
</td>
<td width="60%">
The specified address is not a valid socket address, or no transport provider supports the indicated address family.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(WSANOTINITIALISED)</b></dt>
</dl>
</td>
<td width="60%">
The Winsock 2 DLL has not been initialized. The application must first call <a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> to initialize Winsock 2.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(WSAENOBUFS)</b></dt>
</dl>
</td>
<td width="60%">
No buffer space available.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a>
 

 

