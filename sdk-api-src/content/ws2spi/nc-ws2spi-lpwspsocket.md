---
UID: NC:ws2spi.LPWSPSOCKET
title: LPWSPSOCKET (ws2spi.h)
author: windows-sdk-content
description: The WSPSocket function creates a socket.
old-location: winsock\wspsocket_2.htm
tech.root: WinSock
ms.assetid: 16735fd1-289d-425a-8ad2-c20d73888b1b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPWSPSOCKET, WSPSocket, WSPSocket function [Winsock], _win32_wspsocket_2, winsock.wspsocket_2, ws2spi/WSPSocket
ms.topic: callback
req.header: ws2spi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WSPSocket
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPWSPSOCKET callback function


## -description


The 
<b>WSPSocket</b> function creates a socket.


## -parameters




### -param af [in]

Address family specification.


### -param type [in]

Type specification for the new socket.


### -param protocol [in]

Protocol to be used with the socket that is specific to the indicated address family.


### -param lpProtocolInfo [in]

Pointer to a 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure that defines the characteristics of the socket to be created.


### -param g [in]

Reserved.


### -param dwFlags

Socket attribute specification.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If no error occurs, 
<b>WSPSocket</b> returns a descriptor referencing the new socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address family is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
Blocking Windows Sockets call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEMFILE</a></b></dt>
</dl>
</td>
<td width="60%">
No more socket descriptors are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEPROTONOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified protocol is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEPROTOTYPE</a></b></dt>
</dl>
</td>
<td width="60%">
The specified protocol is the wrong type for this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAESOCKTNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified socket type is not supported in this address family.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>g</i> specified is not valid.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The 
<b>WSPSocket</b> function causes a socket descriptor and any related resources to be allocated. By default, the created socket will not have the overlapped attribute. Windows Sockets providers are encouraged to be realized as Windows installable file systems, and supply system file handles as socket descriptors. These providers must call 
<a href="https://msdn.microsoft.com/f58971eb-0948-4e16-a767-1d4cba9ec721">WPUModifyIFSHandle</a> prior to returning from this function. For nonfile-system Windows Sockets providers, 
<a href="https://msdn.microsoft.com/ecbf9d8b-b705-4160-ac77-afa5b1501534">WPUCreateSocketHandle</a> must be used to acquire a unique socket descriptor from the Ws2_32.dll prior to returning from this function. See  
<a href="https://msdn.microsoft.com/ed5e10f4-fa17-4a07-9cac-43767915b8e9">Descriptor Allocation</a> for more information.

The values for <i>af</i>, <i>type</i>, and <i>protocol</i> are those supplied by the application in the corresponding API functions 
<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> or 
<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a>. A service provider is free to ignore or pay attention to any or all of these values as is appropriate for the particular protocol. However, the provider must be willing to accept the value of zero for <i>af</i> and <i>type</i>, since the Ws2_32.dll considers these to be wildcard values. Also the value of manifest constant <b>FROM_PROTOCOL_INFO</b> must be accepted for any of <i>af</i>, <i>type</i>, and <i>protocol</i>. This value indicates that the Windows Sockets 2 application needs to use the corresponding values from the 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure (<b>iAddressFamily</b>, <b>iSocketType</b>, <b>iProtocol</b>).

The <i>dwFlags</i> parameter can be used to specify the attributes of the socket by using the bitwise <b>OR</b> operator with any of the following flags.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>WSA_FLAG_OVERLAPPED</td>
<td>This flag causes an overlapped socket to be created. Overlapped sockets can utilize 
<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a>, 
<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a>, 
<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a>, 
<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a> and 
<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a> for overlapped I/O operations, which allow multiple operations to be initiated and in process simultaneously. All functions that allow overlapped operations also support nonoverlapped usage on an overlapped socket if the values for parameters related to overlapped operation are null.</td>
</tr>
<tr>
<td>WSA_FLAG_MULTIPOINT_C_ROOT</td>
<td>Indicates that the socket created will be a c_root in a multipoint session. Only allowed if a rooted control plane is indicated in the protocol's 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure.</td>
</tr>
<tr>
<td>WSA_FLAG_MULTIPOINT_C_LEAF</td>
<td>Indicates that the socket created will be a c_leaf in a multicast session. Only allowed if XP1_SUPPORT_MULTIPOINT is indicated in the protocol's 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure.</td>
</tr>
<tr>
<td>WSA_FLAG_MULTIPOINT_D_ROOT</td>
<td>Indicates that the socket created will be a d_root in a multipoint session. Only allowed if a rooted data plane is indicated in the protocol's 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure.</td>
</tr>
<tr>
<td>WSA_FLAG_MULTIPOINT_D_LEAF</td>
<td>Indicates that the socket created will be a d_leaf in a multipoint session. Only allowed if XP1_SUPPORT_MULTIPOINT is indicated in the protocol's 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure.</td>
</tr>
</table>
 


<div> </div>


<div class="alert"><b>Note</b>  For multipoint sockets, exactly one  WSA_FLAG_MULTIPOINT_C_ROOT or WSA_FLAG_MULTIPOINT_C_LEAF must be specified, and exactly one of WSA_FLAG_MULTIPOINT_D_ROOT or WSA_FLAG_MULTIPOINT_D_LEAF must be specified. Refer to 
<a href="https://msdn.microsoft.com/861f457c-fe7e-4128-a3f3-786424a96ea5">Protocol-Independent Multicast and Multipoint in the SPI</a> for additional information.</div>
<div> </div>
Connection-oriented sockets such as SOCK_STREAM provide full-duplex connections, and must be in a connected state before any data can be sent or received on them. A connection to another socket is created with a 
<a href="https://msdn.microsoft.com/1daca98e-57d8-47f1-af5f-778a33b2c538">WSPConnect</a> call. Once connected, data can be transferred using 
<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a> and 
<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a> calls. When a session has been completed, a 
<a href="https://msdn.microsoft.com/0190f561-68fa-45d8-9702-3caae58bf0cc">WSPCloseSocket</a> must be performed.

The communications protocols used to implement a reliable, connection-oriented socket ensure that data is not lost or duplicated. If data for which the peer protocol has buffer space cannot be successfully transmitted within a reasonable length of time, the connection is considered broken and subsequent calls will fail with the error code set to <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAETIMEDOUT</a>.

Connectionless, message-oriented sockets allow sending and receiving of datagrams to and from arbitrary peers using 
<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a> and 
<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>. If such a socket is connected by using 
<a href="https://msdn.microsoft.com/1daca98e-57d8-47f1-af5f-778a33b2c538">WSPConnect</a> to a specific peer, datagrams can be sent to that peer using 
<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a> and can be received from (only) this peer using 
<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a>.

Support for sockets with type <b>SOCK RAW</b> is not required but service providers are encouraged to support raw sockets whenever it makes sense to do so.



A layered service provider supplies an implementation of this function, but it is also a client of this function if and when it calls 
<b>WSPSocket</b> of the next layer in the protocol chain. Some special considerations apply to this function's <i>lpProtocolInfo</i> parameter as it is propagated down through the layers of the protocol chain.

If the next layer in the protocol chain is another layer then when the next layer's 
<b>WSPSocket</b> is called, this layer must pass to the next layer a <i>lpProtocolInfo</i> that references the same unmodified 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure with the same unmodified chain information. However, if the next layer is the base protocol (that is, the last element in the chain), this layer performs a substitution when calling the base provider's 
<b>WSPSocket</b>. In this case, the base provider's 
<b>WSAPROTOCOL_INFO</b> structure should be referenced by the <i>lpProtocolInfo</i> parameter.

One vital benefit of this policy is that base service providers do not have to be aware of protocol chains.

This same propagation policy applies when propagating a 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure through a layered sequence of other functions such as 
<a href="https://msdn.microsoft.com/7a6d8f77-7235-4cd1-90e1-9b5260137246">WSPAddressToString</a>, 
<a href="https://msdn.microsoft.com/6d9cf472-357e-4226-b53e-09083b42ed13">WSPDuplicateSocket</a>, 
<a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a>, or 
<a href="https://msdn.microsoft.com/65cf8f7e-7ef0-472c-82d8-e8f7df9976a9">WSPStringToAddress</a>.




## -see-also




<a href="https://msdn.microsoft.com/ecbf9d8b-b705-4160-ac77-afa5b1501534">WPUCreateSocketHandle</a>



<a href="https://msdn.microsoft.com/d73aa3a8-cef5-485d-b2ba-b2fe42ab6200">WSPAccept</a>



<a href="https://msdn.microsoft.com/0fe5a66a-1126-494c-b4da-8041841685c6">WSPBind</a>



<a href="https://msdn.microsoft.com/1daca98e-57d8-47f1-af5f-778a33b2c538">WSPConnect</a>



<a href="https://msdn.microsoft.com/8e5ff6dc-f24f-4418-8de8-356f74a37eaa">WSPGetSockName</a>



<a href="https://msdn.microsoft.com/ec63c7a5-2cee-4bdf-ab24-a91d2ea9eb5e">WSPGetSockOpt</a>



<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a>



<a href="https://msdn.microsoft.com/43d588dd-7aa2-405b-8f9d-b167bbbc6574">WSPListen</a>



<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a>



<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>



<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a>



<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a>



<a href="https://msdn.microsoft.com/2b440208-ca10-424a-8f18-3241b4e0184c">WSPSetSockOpt</a>



<a href="https://msdn.microsoft.com/b2de40a5-6978-43a6-aa1c-35c10284f09c">WSPShutdown</a>
 

 

