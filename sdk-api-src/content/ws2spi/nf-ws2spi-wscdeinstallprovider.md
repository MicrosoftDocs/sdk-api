---
UID: NF:ws2spi.WSCDeinstallProvider
title: WSCDeinstallProvider function (ws2spi.h)
author: windows-sdk-content
description: Removes the specified transport provider from the system configuration database.
old-location: winsock\wscdeinstallprovider_2.htm
tech.root: WinSock
ms.assetid: 9a2afd11-1944-491f-9c92-9dbac6b3b28e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSCDeinstallProvider, WSCDeinstallProvider function [Winsock], _win32_wscdeinstallprovider_2, winsock.wscdeinstallprovider_2, ws2spi/WSCDeinstallProvider
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
 - WSCDeinstallProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WSCDeinstallProvider function


## -description


The 
<b>WSCDeinstallProvider</b> function removes the specified transport provider from the system configuration database.


## -parameters




### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the provider. This value is stored within each 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure.


### -param lpErrno [out]

A pointer to the error code if the function fails.


## -returns



If no error occurs, 
<b>WSCDeinstallProvider</b> returns zero. Otherwise, it returns <b>SOCKET_ERROR</b>, and a specific error code is available in <i>lpErrno</i>.



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
The <i>lpErrno</i> parameter is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the user lacks the administrative privileges required to write to the  Windows Sockets registry, or a failure occurred when opening a catalog entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
 Insufficient memory was available. This error is returned when there is insufficient memory to allocate a new catalog entry.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSCDeinstallProvider</b> function removes the common Windows Sockets 2 configuration information for the specified provider. After this routine completes successfully, the configuration information stored in the registry will be changed. However, any Ws2_32.dll instances currently in memory will not be able to recognize this change.

On success, <b>WSCDeinstallProvider</b> will attempt to alert all interested applications that have registered for notification of the change by calling <a href="https://msdn.microsoft.com/abaf367a-8f99-478c-a58c-d57e9f9cd8a1">WSAProviderConfigChange</a>.

The <b>WSCDeinstallProvider</b> function can only be called by a user logged on as a member of the Administrators group. If <b>WSCDeinstallProvider</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>WSANO_RECOVERY</b> is returned in the <i>lpErrno</i> parameter. 
 

For computers running Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to <b>requireAdministrator</b>. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



The caller of this function must remove any additional files or service provider–specific configuration information that is needed to completely uninstall the service provider.




## -see-also




<a href="https://msdn.microsoft.com/abaf367a-8f99-478c-a58c-d57e9f9cd8a1">WSAProviderConfigChange</a>



<a href="https://msdn.microsoft.com/c2e5332f-3327-4624-96b4-8e321795961d">WSCEnumProtocols</a>



<a href="https://msdn.microsoft.com/c0736018-2bcf-4281-aa73-3e1ff9eac92e">WSCInstallProvider</a>
 

 

