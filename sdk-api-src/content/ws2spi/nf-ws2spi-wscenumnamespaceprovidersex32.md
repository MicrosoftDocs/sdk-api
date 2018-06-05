---
UID: NF:ws2spi.WSCEnumNameSpaceProvidersEx32
title: WSCEnumNameSpaceProvidersEx32 function
author: windows-sdk-content
description: Retrieves information on available 32-bit namespace providers.
old-location: winsock\wscenumnamespaceprovidersex32.htm
old-project: WinSock
ms.assetid: 544120b2-7575-4deb-8429-2bd4582eceef
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: WSCEnumNameSpaceProvidersEx32, WSCEnumNameSpaceProvidersEx32 function [Winsock], winsock.wscenumnamespaceprovidersex32, ws2spi/WSCEnumNameSpaceProvidersEx32
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ws2_32.dll
api_name:
-	WSCEnumNameSpaceProvidersEx32
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSCEnumNameSpaceProvidersEx32 function


## -description


The 
<b>WSCEnumNameSpaceProvidersEx32</b> function retrieves information on available 32-bit namespace providers.


## -parameters




### -param lpdwBufferLength [in, out]

On input, the number of bytes contained in the buffer pointed to by <i>lpnspBuffer</i>. On output (if the function fails, and the error is 
<a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a>), the minimum number of bytes to allocate for the <i>lpnspBuffer</i> buffer to allow it to retrieve all the requested information. The buffer passed to <b>WSCEnumNameSpaceProvidersEx32</b> must be sufficient to hold all of the namespace information.


### -param lpnspBuffer [out]

A buffer that is filled with 
<a href="https://msdn.microsoft.com/3f4a8916-9db9-4b65-982f-4cb4ec2205ed">WSANAMESPACE_INFOEXW</a> structures. The returned structures are located consecutively at the head of the buffer. Variable sized information referenced by pointers in the structures point to locations within the buffer located between the end of the fixed sized structures and the end of the buffer. The number of structures filled in is the return value of 
<b>WSCEnumNameSpaceProvidersEx32</b>.


## -returns



The 
<b>WSCEnumNameSpaceProvidersEx32</b> function returns the number of 
<a href="https://msdn.microsoft.com/3f4a8916-9db9-4b65-982f-4cb4ec2205ed">WSANAMESPACE_INFOEXW</a> structures copied into <i>lpnspBuffer</i>. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The buffer length was too small to receive all the relevant 
<a href="https://msdn.microsoft.com/3f4a8916-9db9-4b65-982f-4cb4ec2205ed">WSANAMESPACE_INFOEXW</a> structures and associated information or the <i>lpnspBuffer</i> parameter was a <b>NULL</b> pointer. When this error is returned, the buffer length required is returned in the <i>lpdwBufferLength</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>
 




## -remarks



<b>WSCEnumNameSpaceProvidersEx32</b> is a strictly 32-bit version of <a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

  Currently, the only namespace included with Windows that uses information in the <b>ProviderSpecific</b> member of the <a href="https://msdn.microsoft.com/3f4a8916-9db9-4b65-982f-4cb4ec2205ed">WSANAMESPACE_INFOEXW</a> structure are namespace providers for the NS_EMAIL namespace. The format of the <b>ProviderSpecific</b> member for an NS_EMAIL namespace provider is a <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure.

The 32-bit SPI function is equivalent to the native API function (<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>) because there is no concept of a "hidden" namespace provider.

The provider-specific data blob associated with namespace entry
                     passed in the <i>lpProviderInfo</i> parameter to the <a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a> function can be queried using <b>WSCEnumNameSpaceProvidersEx32</b> function.




## -see-also




<a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>



<a href="https://msdn.microsoft.com/3f4a8916-9db9-4b65-982f-4cb4ec2205ed">WSANAMESPACE_INFOEXW</a>



<a href="https://msdn.microsoft.com/792737d9-231d-4524-b1a6-b9904951d5b4">WSCEnumNameSpaceProviders32</a>



<a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a>
 

 

