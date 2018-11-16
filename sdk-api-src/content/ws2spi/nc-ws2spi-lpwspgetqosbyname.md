---
UID: NC:ws2spi.LPWSPGETQOSBYNAME
title: LPWSPGETQOSBYNAME
author: windows-sdk-content
description: The WSPGetQOSByName function initializes a QOS structure based on a named template, or retrieves an enumeration of the available template names.
old-location: winsock\wspgetqosbyname_2.htm
tech.root: WinSock
ms.assetid: 2e218a9b-6db5-4c5a-94e1-207886c401a5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: LPWSPGETQOSBYNAME, WSPGetQOSByName, WSPGetQOSByName function [Winsock], _win32_wspgetqosbyname_2, winsock.wspgetqosbyname_2, ws2spi/WSPGetQOSByName
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WSPGetQOSByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPWSPGETQOSBYNAME callback function


## -description


The 
<i>WSPGetQOSByName</i> function initializes a 
<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure based on a named template, or retrieves an enumeration of the available template names.


## -parameters




### -param s [in]

Descriptor identifying a socket.


### -param lpQOSName [in, out]

Specifies the QOS template name, or supplies a buffer to retrieve an enumeration of the available template names.


### -param lpQOS [out]

Pointer to the <a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure to be filled.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpQOS</i> argument is not a valid part of the user address space, or the buffer length for <i>lpQOS</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified QOS template name is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



Clients can use 
<i>WSPGetQOSByName</i> to initialize a 
<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure to a set of known values appropriate for a particular service class or media type. These values are stored in a template that is referenced by a well-known name. The client may retrieve these values by setting the <b>buf</b> member of the 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> indicated by <i>lpQOSName</i> to point to a Unicode string of nonzero length specifying a template name. In this case the usage of <i>lpQOSName</i> is IN only, and results are returned through <i>lpQOS</i>.

Alternatively, the client may use 
<b>WSPGetQOSByName</b> to retrieve an enumeration of available template names. The client may do this by setting the <b>buf</b> member of the 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> indicated by <i>lpQOSName</i> to a zero-length null-terminated Unicode string. In this case, the buffer indicated by <b>buf</b> is overwritten with a sequence of as many null-terminated Unicode template name strings as are available up to the number of bytes available in <b>buf</b> as indicated by the <b>len</b> member of the 
<b>WSABUF</b> indicated by <i>lpQOSName</i>. The list of names itself is terminated by a zero-length Unicode name string. When 
<b>WSPGetQOSByName</b> is used to retrieve template names, the <i>lpQOS</i> parameter is ignored.




## -see-also




<a href="https://msdn.microsoft.com/d73aa3a8-cef5-485d-b2ba-b2fe42ab6200">WSPAccept</a>



<a href="https://msdn.microsoft.com/1daca98e-57d8-47f1-af5f-778a33b2c538">WSPConnect</a>



<a href="https://msdn.microsoft.com/ec63c7a5-2cee-4bdf-ab24-a91d2ea9eb5e">WSPGetSockOpt</a>
 

 

