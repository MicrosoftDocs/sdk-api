---
UID: NF:ws2spi.WPUGetProviderPath
title: WPUGetProviderPath function (ws2spi.h)
description: The WPUGetProviderPath function retrieves the DLL path for the specified provider.
helpviewer_keywords: ["WPUGetProviderPath","WPUGetProviderPath function [Winsock]","_win32_wpugetproviderpath_2","winsock.wpugetproviderpath_2","ws2spi/WPUGetProviderPath"]
old-location: winsock\wpugetproviderpath_2.htm
tech.root: WinSock
ms.assetid: fb59e69a-bee4-4807-9ef2-cbcc8c0d367f
ms.date: 12/05/2018
ms.keywords: WPUGetProviderPath, WPUGetProviderPath function [Winsock], _win32_wpugetproviderpath_2, winsock.wpugetproviderpath_2, ws2spi/WPUGetProviderPath
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
 - WPUGetProviderPath
 - ws2spi/WPUGetProviderPath
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
 - WPUGetProviderPath
---

# WPUGetProviderPath function


## -description

The 
**WPUGetProviderPath** function retrieves the DLL path for the specified provider.

## -parameters

### -param lpProviderId [in]

Locally unique identifier of the provider. This must be a value obtained by using 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>.

### -param lpszProviderDllPath [out]

Pointer to a buffer containing a string that identifies the provider DLL's path. This path is a null-terminated string and any embedded environment strings (such as %SystemRoot%) have not been expanded.

### -param lpProviderDllPathLen [in, out]

Size of the buffer pointed to by <i>lpszProviderDllPath</i>, in characters.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
**WPUGetProviderPath** returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter does not specify a valid provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
Either <i>lpszProviderDllPath</i> or <i>lpErrno</i> is not in a valid part of the user address space, or <i>lpProviderDllPathLen</i> is too small.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
**WPUGetProviderPath** function retrieves the DLL path for the specified provider. The DLL path is null-terminated and may contain embedded environment strings (such as %SystemRoot%). Thus, the string should be expanded prior to being used with <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>. For more information, see **LoadLibrary**.

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallprovider">WSCInstallProvider</a>

