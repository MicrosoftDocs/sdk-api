---
UID: NF:ws2spi.WSCGetProviderPath
title: WSCGetProviderPath function (ws2spi.h)
author: windows-sdk-content
description: The WSCGetProviderPath function retrieves the DLL path for the specified provider.
old-location: winsock\wscgetproviderpath_2.htm
tech.root: WinSock
ms.assetid: fe60c8c4-e2d0-48cc-9fdf-e58e408fb1b3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSCGetProviderPath, WSCGetProviderPath function [Winsock], _win32_wscgetproviderpath_2, winsock.wscgetproviderpath_2, ws2spi/WSCGetProviderPath
ms.topic: function
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSCGetProviderPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSCGetProviderPath function


## -description


The 
<b>WSCGetProviderPath</b> function retrieves the DLL path for the specified provider.


## -parameters




### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the provider. This value is obtained by using 
<a href="https://msdn.microsoft.com/c2e5332f-3327-4624-96b4-8e321795961d">WSCEnumProtocols</a>.


### -param lpszProviderDllPath [out]

A pointer to a buffer into which the provider DLL's path string is returned. The path is a null-terminated string and any embedded environment strings, such as %SystemRoot%, have not been expanded.


### -param lpProviderDllPathLen [in, out]

The size, in characters, of the buffer pointed to by the <i>lpszProviderDllPath</i> parameter.


### -param lpErrno [out]

A pointer to the error code if the function fails.


## -returns



If no error occurs, 
<b>WSCGetProviderPath</b> returns zero. Otherwise, it returns SOCKET_ERROR. The specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter does not specify a valid provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszProviderDllPath</i> or <i>lpErrno</i> parameter is not in a valid part of the user address space, or <i>lpProviderDllPathLen</i> is too small.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSCGetProviderPath</b> function retrieves the DLL path for the specified provider. The DLL path can contain embedded environment strings, such as %SystemRoot%, and thus should be expanded prior to being used with the Windows <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function. For more information, see <b>LoadLibrary</b>.




## -see-also




<a href="https://msdn.microsoft.com/c2e5332f-3327-4624-96b4-8e321795961d">WSCEnumProtocols</a>



<a href="https://msdn.microsoft.com/c0736018-2bcf-4281-aa73-3e1ff9eac92e">WSCInstallProvider</a>
 

 

