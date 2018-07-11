---
UID: NF:ws2spi.WSCEnumNameSpaceProviders32
title: WSCEnumNameSpaceProviders32 function
author: windows-sdk-content
description: Returns information on available 32-bit namespace providers.Note  This call is a strictly 32-bit version of WSAEnumNameSpaceProviders for use on 64-bit platforms. It is provided to allow 64-bit processes to access the 32-bit catalogs. .
old-location: winsock\wscenumnamespaceproviders32.htm
old-project: WinSock
ms.assetid: 792737d9-231d-4524-b1a6-b9904951d5b4
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: WSCEnumNameSpaceProviders32, WSCEnumNameSpaceProviders32 function [Winsock], winsock.wscenumnamespaceproviders32, ws2spi/WSCEnumNameSpaceProviders32
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
tech.root: 
req.typenames: WSC_PROVIDER_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSCEnumNameSpaceProviders32
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSCEnumNameSpaceProviders32 function


## -description


The <b>WSCEnumNameSpaceProviders32</b> function returns information on available 32-bit namespace providers.<div class="alert"><b>Note</b>  This call is a strictly 32-bit version of <a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a> for use on 64-bit platforms. It is provided to allow 64-bit processes to access the 32-bit catalogs.</div>
<div> </div>



## -parameters




### -param lpdwBufferLength [in, out]

On input, the number of bytes contained in the buffer pointed to by <i>lpnspBuffer</i>. On output (if the function fails, and the error is 
<a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEFAULT</a>), the minimum number of bytes to allocate for the <i>lpnspBuffer</i> buffer to allow it to retrieve all the requested information. The buffer passed to <b>WSCEnumNameSpaceProviders32</b> must be sufficient to hold all of the namespace information.


### -param lpnspBuffer [out]

A buffer that is filled with 
<a href="https://msdn.microsoft.com/a5c76657-df62-471a-95e9-8017cad47b00">WSANAMESPACE_INFOW</a> structures. The returned structures are located consecutively at the head of the buffer. Variable sized information referenced by pointers in the structures point to locations within the buffer located between the end of the fixed sized structures and the end of the buffer. The number of structures filled in is the return value of 
<b>WSCEnumNameSpaceProviders32</b>.


## -returns



The 
<b>WSCEnumNameSpaceProviders32</b> function returns the number of 
<a href="https://msdn.microsoft.com/a5c76657-df62-471a-95e9-8017cad47b00">WSANAMESPACE_INFOW</a> structures copied into <i>lpnspBuffer</i>. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpnspBuffer</i> parameter was a <b>NULL</b> pointer or the buffer length, <i>lpdwBufferLength</i>, was too small to receive all the relevant 
<a href="https://msdn.microsoft.com/a5c76657-df62-471a-95e9-8017cad47b00">WSANAMESPACE_INFOW</a> structures and associated information. When this error is returned, the buffer length required is returned in the <i>lpdwBufferLength</i> parameter. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>
 




## -remarks



<b>WSCEnumNameSpaceProviders32</b> is a strictly 32-bit version of <a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

The 32-bit SPI function is equivalent to the native API function (<a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>) because there is no concept of a "hidden" namespace provider.

The <b>WSCEnumNameSpaceProviders32</b> function is a Unicode only function and returns <a href="https://msdn.microsoft.com/3f4a8916-9db9-4b65-982f-4cb4ec2205ed">WSANAMESPACE_INFOEXW</a> structures. 




## -see-also




<a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>



<a href="https://msdn.microsoft.com/a5c76657-df62-471a-95e9-8017cad47b00">WSANAMESPACE_INFOW</a>



<a href="https://msdn.microsoft.com/b107fbe6-bbfb-45be-8419-4d85d3c4e80c">WSCInstallNameSpace32</a>



<a href="https://msdn.microsoft.com/13dde602-c958-4312-a16f-a393dd6fb829">WSCInstallNameSpaceEx32</a>
 

 

