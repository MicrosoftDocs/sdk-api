---
UID: NF:winsock2.WSAGetQOSByName
title: WSAGetQOSByName function
author: windows-sdk-content
description: The WSAGetQOSByName function initializes a QOS structure based on a named template, or it supplies a buffer to retrieve an enumeration of the available template names.
old-location: winsock\wsagetqosbyname_2.htm
old-project: winsock
ms.assetid: 9b586856-5441-414b-8b91-298c952c351b
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: WSAGetQOSByName, WSAGetQOSByName function [Winsock], _win32_wsagetqosbyname_2, winsock.wsagetqosbyname_2, winsock2/WSAGetQOSByName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
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
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAGetQOSByName
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAGetQOSByName function


## -description


The 
<b>WSAGetQOSByName</b> function initializes a 
<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure based on a named template, or it supplies a buffer to retrieve an enumeration of the available template names.


## -parameters




### -param s [in]

A descriptor identifying a socket.


### -param lpQOSName [in, out]

A pointer to a specific quality of service template.


### -param lpQOS [out]

A pointer to the 
<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure to be filled.


## -returns



If 
<b>WSAGetQOSByName</b> succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.

</td>
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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpQOSName</i> or <i>lpQOS</i> parameter are not a valid part of the user address space, or the buffer length for <i>lpQOS</i> is too small.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAGetQOSByName</b> function is used by applications to initialize a 
<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure to a set of known values appropriate for a particular service class or media type. These values are stored in a template that is referenced by a well-known name. The client may retrieve these values by setting the <i>buf</i> parameter of the 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structure indicated by <i>lpQOSName</i>, which points to a string of nonzero length specifying a template name. In this case, the usage of <i>lpQOSName</i> is IN only, and results are returned through <i>lpQOS</i>.

Alternatively, the client may use this function to retrieve an enumeration of available template names. The client may do this by setting the <i>buf</i> parameter of the 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> indicated by <i>lpQOSName</i> to a zero-length null-terminated string. In this case the buffer indicated by <i>buf</i> is overwritten with a sequence of as many available, null-terminated template names up to the number of bytes available in <i>buf</i> as indicated by the <i>len</i> parameter of the 
<b>WSABUF</b> indicated by <i>lpQOSName</i>. The list of names itself is terminated by a zero-length name. When the 
<b>WSAGetQOSByName</b> function is used to retrieve template names, the <i>lpQOS</i> parameter is ignored.




## -see-also




<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a>



<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a>



<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>
 

 

