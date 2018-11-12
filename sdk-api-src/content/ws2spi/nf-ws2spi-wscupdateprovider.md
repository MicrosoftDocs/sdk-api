---
UID: NF:ws2spi.WSCUpdateProvider
title: WSCUpdateProvider function
author: windows-sdk-content
description: Modifies the specified transport provider in the system configuration database.
old-location: winsock\wscupdateprovider_2.htm
tech.root: winsock
ms.assetid: 7777a2ff-2ece-4f28-88af-87fc96fdda9f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WSCUpdateProvider, WSCUpdateProvider function [Winsock], _win32_wscupdateprovider_2, winsock.wscupdateprovider_2, ws2spi/WSCUpdateProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - WSCUpdateProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSCUpdateProvider function


## -description


The 
<b>WSCUpdateProvider</b> function modifies the specified transport provider in the system configuration database.


## -parameters




### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the provider.


### -param lpszProviderDllPath [in]

A pointer to a Unicode string that contains the load path to the provider 64-bit DLL. This string observes the usual rules for path resolution and can contain embedded environment strings (such as <i>%SystemRoot%</i>). Such environment strings are expanded when the Ws2_32.dll must subsequently load the provider DLL on behalf of an application. After any embedded environment strings are expanded, the Ws2_32.dll passes the resulting string to the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function which loads the provider into memory. For more information, see <b>LoadLibrary</b>.


### -param lpProtocolInfoList [in]

A pointer to an array of 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structures. Each structure specifies or modifies a protocol, address family, and socket type supported by the provider.


### -param dwNumberOfEntries [in]

The number of entries in the <i>lpProtocolInfoList</i> array.


### -param lpErrno [out]

A pointer to the error code if the function fails.


## -returns



If no error occurs, 
<b>WSCUpdateProvider</b> returns zero. Otherwise, it returns <b>SOCKET_ERROR</b>, and a specific error code is returned in the <i>lpErrno</i> parameter.

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
One or more of the arguments are not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the user lacks the administrative privileges required to write to the  Winsock registry, or a failure occurred when opening or writing a catalog entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
 Insufficient memory was available. This error is returned when there is insufficient memory to allocate a new catalog entry.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSCUpdateProvider</b> function modifies Windows Sockets 2 configuration information for the specified provider. It is applicable to base protocols, layered protocols, and protocol chains.

Winsock 2 accommodates layered protocols. A layered protocol is one that implements only higher level communications functions, while relying on an underlying transport stack for the actual exchange of data with a remote endpoint. An example of a layered protocol would be a security layer that adds protocol to the connection establishment process in order to perform authentication and to establish a mutually agreed upon encryption scheme.  Such a security protocol would generally require the services of an underlying reliable transport protocol such as TCP or SPX.  The term base protocol refers to a protocol such as TCP or SPX which is capable of performing data communications with a remote endpoint. The term layered protocol is used to describe a protocol that cannot stand alone.  A protocol chain would then be defined as one or more layered protocols strung together and anchored by a base protocol.
A base protocol has the <b>ChainLen</b> member of the <a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure set to  <b>BASE_PROTOCOL</b> which is defined to be 1. A layered protocol has the <b>ChainLen</b> member of the <b>WSAPROTOCOL_INFO</b> structure set to <b>LAYERED_PROTOCOL</b> which is defined to be zero. A protocol chain has the <b>ChainLen</b> member of the <b>WSAPROTOCOL_INFO</b> structure set to greater than 1.

On success, <b>WSCUpdateProvider</b> will attempt to alert all interested applications that have registered for notification of the change by calling <a href="https://msdn.microsoft.com/abaf367a-8f99-478c-a58c-d57e9f9cd8a1">WSAProviderConfigChange</a>.

The <b>WSCUpdateProvider</b> function can only be called by a user logged on as a member of the Administrators group. If <b>WSCUpdateProvider</b> is called by a user that is not a member of the Administrators group, the function call will fail. 
 

For computers running on Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to <b>requireAdministrator</b>. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

Any file installation or service provider-specific configuration must be performed by the caller.




## -see-also




<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a>



<a href="https://msdn.microsoft.com/abaf367a-8f99-478c-a58c-d57e9f9cd8a1">WSAProviderConfigChange</a>



<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>



<a href="https://msdn.microsoft.com/9a2afd11-1944-491f-9c92-9dbac6b3b28e">WSCDeinstallProvider</a>



<a href="https://msdn.microsoft.com/c2e5332f-3327-4624-96b4-8e321795961d">WSCEnumProtocols</a>



<a href="https://msdn.microsoft.com/c0736018-2bcf-4281-aa73-3e1ff9eac92e">WSCInstallProvider</a>
 

 

