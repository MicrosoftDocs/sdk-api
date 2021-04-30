---
UID: NC:ws2spi.LPNSPINSTALLSERVICECLASS
title: LPNSPINSTALLSERVICECLASS (ws2spi.h)
description: The NSPInstallServiceClass function registers service class schema within the namespace providers.
helpviewer_keywords: ["LPNSPINSTALLSERVICECLASS","NSPInstallServiceClass","NSPInstallServiceClass function [Winsock]","_win32_nspinstallserviceclass_2","winsock.nspinstallserviceclass_2","ws2spi/NSPInstallServiceClass"]
old-location: winsock\nspinstallserviceclass_2.htm
tech.root: WinSock
ms.assetid: 437a3580-e296-4f20-8921-84e522cccc1a
ms.date: 12/05/2018
ms.keywords: LPNSPINSTALLSERVICECLASS, NSPInstallServiceClass, NSPInstallServiceClass function [Winsock], _win32_nspinstallserviceclass_2, winsock.nspinstallserviceclass_2, ws2spi/NSPInstallServiceClass
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
 - LPNSPINSTALLSERVICECLASS
 - ws2spi/LPNSPINSTALLSERVICECLASS
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
 - NSPInstallServiceClass
---

# LPNSPINSTALLSERVICECLASS callback function


## -description

The 
**NSPInstallServiceClass** function registers service class schema within the namespace providers.

The schema includes the class name, class identifier, and any namespace-specific type information that is common to all instances of the service, such as SAP identifier or object identifier. A dynamic namespace provider is expected to store any class information associated with that namespace.

## -parameters

### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider that this service class schema is registered in.

### -param lpServiceClassInfo [in]

A pointer to the service class schema information.

## -returns

The function should return **NO_ERROR** (zero) if the routine succeeds. It should return **SOCKET_ERROR** (–1) if the routine fails and it must set the appropriate error code using 
<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_PARAMETER</a></b></dl>
</dl>
</td>
<td width="60%">
The namespace provider cannot supply the requested class information.

</td>
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
The calling routine does not have sufficient privileges to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a></b></dl>
</dl>
</td>
<td width="60%">
The service class information has already been registered for this service class identifier. To modify service class information, first call <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspremoveserviceclass">NSPRemoveServiceClass</a>, then reinstall with updated class information data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The service class identifier was invalid or improperly structured. This error is returned if the <i>lpServiceClassInfo</i> parameter is **NULL**.

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
</table>

## -remarks

Namespace providers are encouraged, but not required, to store information that is specific to the namespace they support.

## -see-also

<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspgetserviceclassinfo">NSPGetServiceClassInfo</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspremoveserviceclass">NSPRemoveServiceClass</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaserviceclassinfow">WSASERVICECLASSINFOW</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>

