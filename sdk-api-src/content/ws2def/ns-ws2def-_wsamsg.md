---
UID: NS:ws2def._WSAMSG
title: "_WSAMSG"
author: windows-sdk-content
description: Used with the WSARecvMsg and WSASendMsg functions to store address and optional control information about connected and unconnected sockets as well as an array of buffers used to store message data.
old-location: winsock\wsamsg_2.htm
old-project: winsock
ms.assetid: 105a6e2c-1edf-4ec0-a1c2-ac0bcafeda30
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: "*LPWSAMSG, *PWSAMSG, LPWSAMSG, LPWSAMSG structure pointer [Winsock], MSG_BCAST, MSG_CTRUNC, MSG_MCAST, MSG_PEEK, MSG_TRUNC, PWSAMSG, PWSAMSG structure pointer [Winsock], WSAMSG, WSAMSG structure [Winsock], _WSAMSG, _win32_wsamsg_2, mswsock/LPWSAMSG, mswsock/PWSAMSG, mswsock/WSAMSG, winsock.wsamsg_2, ws2def/LPWSAMSG, ws2def/PWSAMSG, ws2def/WSAMSG"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2def.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSAMSG, *PWSAMSG, *LPWSAMSG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2def.h
 - Mswsock.h
api_name:
 - WSAMSG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSAMSG structure


## -description



			The 
<b>WSAMSG</b> structure is used with the 
<a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a>  and <a href="https://msdn.microsoft.com/3b2ba645-6a70-4ba2-b4a2-5bde0c7f8d08">WSASendMsg</a> functions to store address and optional control information about connected and unconnected sockets as well as an array of buffers used  to store message data.


## -struct-fields




### -field name

Type: <b>LPSOCKADDR</b>

A pointer to a 
<a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a> structure that stores information about the remote address. Used only with unconnected sockets.


### -field namelen

Type: <b>INT</b>

The length, in bytes, of the 
<a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a> structure pointed to in the <b>pAddr</b> member. Used only with unconnected sockets.


### -field lpBuffers

Type: <b>LPWSABUF</b>

An array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565943">WSABUF</a> structures used to receive the message data. The capability of the <b>lpBuffers</b> member to contain multiple buffers enables the use of scatter/gather I/O.


### -field dwBufferCount

Type: <b>DWORD</b>

The number of buffers pointed to in the <b>lpBuffers</b> member.


### -field Control

Type: <b>WSABUF</b>

A structure of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565943">WSABUF</a> type used to specify optional control data. See Remarks.


### -field dwFlags

Type: <b>DWORD</b>

One or more control flags, specified as the logical <b>OR</b> of values. The possible values for <b>dwFlags</b> member on input are defined in the Winsock2.h header file. The possible values for <b>dwFlags</b> member on output are defined in the Ws2def.h header file which is automatically included by the Winsock2.h header file. 

<table>
<tr>
<th>Flags on input</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSG_PEEK"></a><a id="msg_peek"></a><dl>
<dt><b>MSG_PEEK</b></dt>
</dl>
</td>
<td width="60%">
Peek at the incoming data. The data is copied into the buffer, but is not removed from the input queue. This flag is valid only for non-overlapped sockets.

</td>
</tr>
</table>
 

<table>
<tr>
<th>Flag returned</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSG_BCAST"></a><a id="msg_bcast"></a><dl>
<dt><b>MSG_BCAST</b></dt>
</dl>
</td>
<td width="60%">
The datagram was received as a link-layer broadcast or with a destination IP address that is a broadcast address.

</td>
</tr>
<tr>
<td width="40%"><a id="MSG_MCAST"></a><a id="msg_mcast"></a><dl>
<dt><b>MSG_MCAST</b></dt>
</dl>
</td>
<td width="60%">
The datagram was received with a destination IP address that is a multicast address.

</td>
</tr>
<tr>
<td width="40%"><a id="MSG_TRUNC"></a><a id="msg_trunc"></a><dl>
<dt><b>MSG_TRUNC</b></dt>
</dl>
</td>
<td width="60%">
The datagram was truncated. More data was present than the process allocated room for.

</td>
</tr>
<tr>
<td width="40%"><a id="MSG_CTRUNC"></a><a id="msg_ctrunc"></a><dl>
<dt><b>MSG_CTRUNC</b></dt>
</dl>
</td>
<td width="60%">
The control (ancillary) data was truncated. More control data was present than the process allocated room for.

</td>
</tr>
</table>
 


## -remarks



In the Microsoft Windows Software Development Kit (SDK), the version of this structure for use on Windows Vista
  is defined with the data type for the <b>dwBufferCount</b> and <b>dwFlags</b> members as a <b>ULONG</b>.  When compiling an application if the target platform is Windows Vista and later (<b>NTDDI_VERSION &gt;= NTDDI_LONGHORN, _WIN32_WINNT &gt;= 0x0600</b>, or <b>WINVER &gt;= 0x0600</b>), the data type for the <b>dwBufferCount</b> and <b>dwFlags</b> members is a <b>ULONG</b>.

<b>Windows Server 2003 and Windows XP:  </b> When compiling an application, the data type for the <b>dwBufferCount</b> and <b>dwFlags</b> members is a <b>DWORD</b>.

On the Windows SDK released for Windows Vista and later, the <b>WSAMSG</b> structure is defined in the Ws2def.h header file. Note that the Ws2def.h header file is automatically included in Winsock2.h, and should never be used directly

If the datagram or control data is truncated during the transmission, the function being used in association with the 
<b>WSAMSG</b> structure returns SOCKET_ERROR and a call to the 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function returns WSAEMSGSIZE. It is up to the application to determine what was truncated by checking for MSG_TRUNC and/or MSG_CTRUNC flags.

<h3><a id="Use_of_the_Control_Member"></a><a id="use_of_the_control_member"></a><a id="USE_OF_THE_CONTROL_MEMBER"></a>Use of the Control Member</h3>
The following table summarizes the various uses of control data available for use in the <b>Control</b> member for IPv4 and IPv6.


<table>
<tr>
<th>Protocol</th>
<th>cmsg_level</th>
<th>cmsg_type</th>
<th>Description</th>
</tr>
<tr>
<td>IPv4</td>
<td>IPPROTO_IP</td>
<td>IP_ORIGINAL_ARRIVAL_IF</td>
<td>
Receives the original IPv4 arrival interface where the packet was received for datagram sockets. This control data is used by firewalls when a Teredo, 6to4, or ISATAP tunnel is used for IPv4 NAT traversal.

The cmsg_data[] member in the <b>WSAMSG</b> structure is a <b>ULONG</b> that contains the IF_INDEX defined in the Ifdef.h header file.

For more information, see the <a href="https://msdn.microsoft.com/6b06a29e-59cd-4446-bd2f-131dc25bf571">IPPROTO_IP Socket Options</a> for the IP_ORIGINAL_ARRIVAL_IF socket option.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>The IP_ORIGINAL_ARRIVAL_IF   <b>cmsg_type</b> is not supported.

</td>
</tr>
<tr>
<td>IPv4</td>
<td>IPPROTO_IP</td>
<td>
<a href="https://msdn.microsoft.com/C6246899-0220-4F88-B43B-CED1B1FF7DC3">IP_PKTINFO</a>
</td>
<td>
Specifies/receives packet information for an IPv4 socket.

For more information, see the <a href="https://msdn.microsoft.com/C6246899-0220-4F88-B43B-CED1B1FF7DC3">IP_PKTINFO</a> socket option.

</td>
</tr>
<tr>
<td>IPv6</td>
<td>IPPROTO_IPV6</td>
<td>IPV6_DSTOPTS</td>
<td>
Specifies/receives destination options.

</td>
</tr>
<tr>
<td>IPv6</td>
<td>IPPROTO_IPV6</td>
<td>IPV6_HOPLIMIT</td>
<td>
Specifies/receives hop limit.

For more information, see the <a href="https://msdn.microsoft.com/65f8f7a4-757b-43a3-9d47-b115754c89d6">IPPROTO_IPV6 Socket Options</a> for the IPV6_HOPLIMIT socket option.

</td>
</tr>
<tr>
<td>IPv6</td>
<td>IPPROTO_IPV6</td>
<td>IPV6_HOPOPTS</td>
<td>
Specifies/receives hop-by-hop options.

</td>
</tr>
<tr>
<td>IPv6</td>
<td>IPPROTO_IPV6</td>
<td>IPV6_NEXTHOP</td>
<td>
Specifies next-hop address.

</td>
</tr>
<tr>
<td>IPv6</td>
<td>IPPROTO_IPV6</td>
<td>
<a href="https://msdn.microsoft.com/7BF17538-BE92-44FE-BA3C-6B44F61D478A">IPV6_PKTINFO</a>
</td>
<td>
Specifies/receives packet information for an IPv6 socket.

For more information, see the <a href="https://msdn.microsoft.com/7BF17538-BE92-44FE-BA3C-6B44F61D478A">IPV6_PKTINFO</a> socket option.

</td>
</tr>
<tr>
<td>IPv6</td>
<td>IPPROTO_IPV6</td>
<td>IPV6_RTHDR</td>
<td>
Specifies/receives routing header.

</td>
</tr>
</table>
 



Control data is made up of one or more control data objects, each beginning with a <b>WSACMSGHDR</b> structure, defined as the following.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
struct wsacmsghdr {
  UINT        cmsg_len;
  INT         cmsg_level;
  INT         cmsg_type;
  /* followed by UCHAR cmsg_data[] */
} WSACMSGHDR;
</pre>
</td>
</tr>
</table></span></div>

<div class="alert"><b>Note</b>  The transport, not the application, fills out the header information in the <b>WSACMSGHDR</b> structure. The application simply sets the needed socket options and provides the adequate buffer size.</div>
<div> </div>


The members of the <b>WSACMSGHDR</b> structure are as follows:




<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="cmsg_len"></a><a id="CMSG_LEN"></a>cmsg_len

</td>
<td width="60%">
The number of bytes of data starting from the beginning of the <b>WSACMSGHDR</b> to the end of data (excluding padding bytes that may follow data). 

</td>
</tr>
<tr>
<td width="40%">
<a id="cmsg_level"></a><a id="CMSG_LEVEL"></a>cmsg_level

</td>
<td width="60%">
The protocol that originated the control information. 

</td>
</tr>
<tr>
<td width="40%">
<a id="cmsg_type"></a><a id="CMSG_TYPE"></a>cmsg_type

</td>
<td width="60%">
The protocol-specific type of control information.

</td>
</tr>
</table>
 



The following macros are used to navigate the data objects:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define LPCMSGHDR *WSA_CMSG_FIRSTHDR(LPWSAMSG msg);
</pre>
</td>
</tr>
</table></span></div>
Returns a pointer to the first control data object. Returns a <b>NULL</b> pointer if there is no control data in the 
<b>WSAMSG</b> structure, such as when the <b>Control</b> member is a <b>NULL</b> pointer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define LPCMSGHDR *WSA_CMSG_NXTHDR(LPWSAMSG msg, LPWSACMSGHDR cmsg);
</pre>
</td>
</tr>
</table></span></div>
Returns a pointer to the next control data object, or <b>NULL</b> if there are no more data objects. If the  <i>pcmsg</i> parameter is <b>NULL</b>, a pointer to the first control data object is returned.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define UCHAR *WSA_CMSG_DATA(LPWSACMSGHDR pcmsg);
</pre>
</td>
</tr>
</table></span></div>
Returns a pointer to the first byte of data (referred to as the <b>cmsg_data</b> member, though it is not defined in the structure).

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define UINT WSA_CMSG_SPACE(UINT length);
</pre>
</td>
</tr>
</table></span></div>
Returns the total size of a control data object, given the amount of data. Used to allocate the correct amount of buffer space. Includes alignment padding.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define UINT WSA_CMSG_LEN(UINT length);
</pre>
</td>
</tr>
</table></span></div>
Returns the value in <b>cmsg_len</b> given the amount of data. Includes alignment padding.




## -see-also




<a href="https://msdn.microsoft.com/7BF17538-BE92-44FE-BA3C-6B44F61D478A">IPV6_PKTINFO</a>



<a href="https://msdn.microsoft.com/C6246899-0220-4F88-B43B-CED1B1FF7DC3">IP_PKTINFO</a>



<a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565943">WSABUF</a>



<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>



<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a>



<a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a>



<a href="https://msdn.microsoft.com/3b2ba645-6a70-4ba2-b4a2-5bde0c7f8d08">WSASendMsg</a>
 

 

