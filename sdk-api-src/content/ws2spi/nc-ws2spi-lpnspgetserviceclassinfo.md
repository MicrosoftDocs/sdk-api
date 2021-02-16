---
UID: NC:ws2spi.LPNSPGETSERVICECLASSINFO
title: LPNSPGETSERVICECLASSINFO (ws2spi.h)
description: Retrieves all the pertinent class information (schema) pertaining to the namespace provider.
helpviewer_keywords: ["LPNSPGETSERVICECLASSINFO","NSPGetServiceClassInfo","NSPGetServiceClassInfo function [Winsock]","_win32_nspgetserviceclassinfo_2","winsock.nspgetserviceclassinfo_2","ws2spi/NSPGetServiceClassInfo"]
old-location: winsock\nspgetserviceclassinfo_2.htm
tech.root: WinSock
ms.assetid: babe1c96-9077-4d91-a52a-839c89d7a83b
ms.date: 12/05/2018
ms.keywords: LPNSPGETSERVICECLASSINFO, NSPGetServiceClassInfo, NSPGetServiceClassInfo function [Winsock], _win32_nspgetserviceclassinfo_2, winsock.nspgetserviceclassinfo_2, ws2spi/NSPGetServiceClassInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPNSPGETSERVICECLASSINFO
 - ws2spi/LPNSPGETSERVICECLASSINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPGetServiceClassInfo
---

## -description

The **NSPGetServiceClassInfo** function retrieves all the pertinent class information (schema) pertaining to the namespace provider. This call retrieves any namespace-specific information that is common to all instances of the service, including connection information for SAP, or port information for SAP or TCP.

## -parameters

### -param lpProviderId [in]

A pointer to the [GUID](../guiddef/ns-guiddef-guid.md) of the specific namespace provider from which the service class schema is to be retrieved.

### -param lpdwBufSize [in, out]

On input, the size, in bytes, of the buffer pointed to by <i>lpServiceClassInfo</i> parameter. 

On output, if the function fails and the error is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a>, this parameter specifies the minimum size, in bytes, of the buffer pointed to the <i>lpServiceClassInfo</i> parameter needed to retrieve the record.

### -param lpServiceClassInfo [in, out]

Returns a pointer to <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFOW</a> structure that contains the service class to namespace-specific mapping information. The <i>lpServiceClassId</i> parameter must be filled to indicate which **WSASERVICECLASSINFOW** record should be returned.

## -returns

If no error occurs, the **NSPGetServiceClassInfo** function returns **NO_ERROR** (zero). Otherwise, **SOCKET_ERROR** (–1) is returned and the namespace provider must set the appropriate error code using <a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dl>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dl>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to access the information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The  buffer pointed to by the <i>lpServiceClass</i> parameter was too small to contain a <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFOW</a> structure. The application needs to pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The specified service class identifier or namespace provider identifier is not valid. This error is returned if the <i>lpProviderId</i>, <i>lpServiceClassId</i>, <i>lpdwBufSize</i>, or <i>lpServiceClassInfo</i> parameters are **NULL**.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a></b></dl>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_DATA</a></b></dl>
</dl>
</td>
<td width="60%">
The requested name is valid, but no data of the requested type was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATYPE_NOT_FOUND</a></b></dl>
</dl>
</td>
<td width="60%">
The specified class was not found.

</td>
</tr>
</table>

## -remarks

The W2_32.dll uses this function to implement the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetserviceclassnamebyclassida">WSAGetServiceClassNameByClassId</a> function, as well as to retrieve the namespace-specific information passed to the 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a> and 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspsetservice">NSPSetService</a> functions.

## -see-also

<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspinstallserviceclass">NSPInstallServiceClass</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspremoveserviceclass">NSPRemoveServiceClass</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspsetservice">NSPSetService</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetserviceclassinfoa">WSAGetServiceClassInfo</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetserviceclassnamebyclassida">WSAGetServiceClassNameByClassId</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFOW</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>