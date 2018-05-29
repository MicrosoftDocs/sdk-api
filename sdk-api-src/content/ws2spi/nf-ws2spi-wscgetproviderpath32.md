---
UID: NF:ws2spi.WSCGetProviderPath32
title: WSCGetProviderPath32 function
author: windows-sdk-content
description: Retrieves the DLL path for the specified 32-bit provider.Note  This call is a strictly 32-bit version of WSCGetProviderPath for use on 64-bit platforms. It is provided to allow 64-bit processes to access the 32-bit catalogs. .
old-location: winsock\wscgetproviderpath32.htm
old-project: WinSock
ms.assetid: fd4ef7da-344d-4825-93b2-f0cd5622aeac
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: WSCGetProviderPath32, WSCGetProviderPath32 function [Winsock], winsock.wscgetproviderpath32, ws2spi/WSCGetProviderPath32
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 x64 Edition [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSC_PROVIDER_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ws2_32.dll
api_name:
-	WSCGetProviderPath32
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSCGetProviderPath32 function


## -description


The <b>WSCGetProviderPath32</b> function retrieves the DLL path for the specified 32-bit provider.<div class="alert"><b>Note</b>  This call is a strictly 32-bit version of <a href="https://msdn.microsoft.com/fe60c8c4-e2d0-48cc-9fdf-e58e408fb1b3">WSCGetProviderPath</a> for use on 64-bit platforms. It is provided to allow 64-bit processes to access the 32-bit catalogs.</div>
<div> </div>



## -parameters




### -param lpProviderId [in]

Locally unique identifier of the provider. This value is obtained by using 
<a href="https://msdn.microsoft.com/f46042f6-0b14-4a14-abc1-4e40c34b1599">WSCEnumProtocols32</a>.


### -param lpszProviderDllPath [out]

Pointer to a buffer into which the provider DLL's path string is returned. The path is a null-terminated string and any embedded environment strings, such as %SystemRoot%, have not been expanded.


### -param lpProviderDllPathLen [in, out]

Size of the buffer pointed to by the <i>lpszProviderDllPath</i> parameter, in characters.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If 
no error occurs, <b>WSCGetProviderPath32</b> returns zero. Otherwise, it returns SOCKET_ERROR. The specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter does not specify a valid provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszProviderDllPath</i> or <i>lpErrno</i> parameter is not in a valid part of the user address space, or <i>lpProviderDllPathLen</i> is too small.

</td>
</tr>
</table>
 




## -remarks



<b>WSCGetProviderPath32</b> is a strictly 32-bit version of <a href="https://msdn.microsoft.com/fe60c8c4-e2d0-48cc-9fdf-e58e408fb1b3">WSCGetProviderPath</a>. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

The 
<b>WSCGetProviderPath32</b> function retrieves the DLL path for the specified provider. The DLL path can contain embedded environment strings, such as %SystemRoot%, and thus should be expanded prior to being used with the Windows <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function. For more information, see <b>LoadLibrary</b>.




## -see-also




<a href="https://msdn.microsoft.com/f46042f6-0b14-4a14-abc1-4e40c34b1599">WSCEnumProtocols32</a>



<a href="https://msdn.microsoft.com/50d3a5d1-18f2-439e-a16c-6f31becb1e65">WSCInstallProvider64_32</a>
 

 

