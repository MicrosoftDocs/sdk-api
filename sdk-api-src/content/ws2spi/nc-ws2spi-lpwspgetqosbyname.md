---
UID: NC:ws2spi.LPWSPGETQOSBYNAME
title: LPWSPGETQOSBYNAME
description: The LPWSPGetQOSByName function initializes a QOS structure based on a named template, or retrieves an enumeration of the available template names.
tech.root: winsock
helpviewer_keywords: ["LPWSPGETQOSBYNAME"]
ms.date: 4/26/2019
ms.keywords: LPWSPGETQOSBYNAME
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ws2spi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - ws2spi.h
api_name:
 - LPWSPGETQOSBYNAME
f1_keywords:
 - LPWSPGETQOSBYNAME
 - ws2spi/LPWSPGETQOSBYNAME
---

## -description

The **WSPGetQOSByName** function initializes a <b><a href="/en-us/previous-versions/windows/desktop/qos/qos-structures">QOS</a></b> structure based on a named template, or retrieves an enumeration of the available template names.

## -parameters

### -param s [in]

Descriptor identifying a socket.

### -param lpQOSName [in, out]

Specifies the QOS template name, or supplies a buffer to retrieve an enumeration of the available template names.

### -param lpQOS [out]

Pointer to the <b><a href="/previous-versions/windows/desktop/qos/qos-structures">QOS</a></b> structure to be filled.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If the function succeeds, the return value is **TRUE**. If the function fails, the return value is **FALSE**, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                      
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></b></dl>
</dl>
</td>
<td width="60%">
The network subsystem has failed.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                      
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTSOCK">WSAENOTSOCK</a></b></dl>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                      
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAENOTSOCK</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpQOS</i> argument is not a valid part of the user address space, or the buffer length for <i>lpQOS</i> is too small.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                      
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The specified QOS template name is invalid.
</td>
</tr>
</table>

## -remarks

Clients can use <i>WSPGetQOSByName</i> to initialize a <b><a href="/previous-versions/windows/desktop/qos/qos-structures">QOS</a></b> structure to a set of known values appropriate for a particular service class or media type. These values are stored in a template that is referenced by a well-known name. The client may retrieve these values by setting the **buf** member of the **WSABUF** indicated by <i>lpQOSName</i> to point to a Unicode string of nonzero length specifying a template name. In this case the usage of <i>lpQOSName</i> is IN only, and results are returned through <i>lpQOS</i>.

Alternatively, the client may use **LPWSPGetQOSByName** to retrieve an enumeration of available template names. The client may do this by setting the **buf** member of the **WSABUF** indicated by <i>lpQOSName</i> to a zero-length null-terminated Unicode string. In this case, the buffer indicated by **buf** is overwritten with a sequence of as many null-terminated Unicode template name strings as are available up to the number of bytes available in **buf** as indicated by the **len** member of the **WSABUF** indicated by <i>lpQOSName</i>. The list of names itself is terminated by a zero-length Unicode name string. When **LPWSPGetQOSByName** is used to retrieve template names, the <i>lpQOS</i> parameter is ignored.

## -see-also

**[LPWSPAccept](nc-ws2spi-lpwspaccept.md)**

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a></b>

