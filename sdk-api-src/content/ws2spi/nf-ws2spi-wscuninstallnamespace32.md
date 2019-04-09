---
UID: NF:ws2spi.WSCUnInstallNameSpace32
title: WSCUnInstallNameSpace32 function (ws2spi.h)
author: windows-sdk-content
description: Uninstalls a specific 32-bit namespace provider.
old-location: winsock\wscuninstallnamespace32.htm
tech.root: WinSock
ms.assetid: a2a08159-6ac0-493d-8f9f-d19aa199a65f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSCUnInstallNameSpace32, WSCUninstallNamespace32, WSCUninstallNamespace32 function [Winsock], winsock.wscuninstallnamespace32, ws2spi/WSCUninstallNamespace32
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
 - WSCUninstallNamespace32
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSCUnInstallNameSpace32 function


## -description


The <b>WSCUnInstallNameSpace32</b> function uninstalls a specific 32-bit namespace provider.<div class="alert"><b>Note</b>  This call is a strictly 32-bit version of <a href="https://msdn.microsoft.com/5267f986-99fc-4e53-9fbb-3850bb9d24cf">WSCUnInstallNameSpace</a> for use on 64-bit platforms. It is provided to allow 64-bit processes to access the 32-bit catalogs.</div>
<div> </div>



## -parameters




### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the name-space provider to be uninstalled.


## -returns



If no error occurs, 
<b>WSCUnInstallNameSpace32</b> returns <b>NO_ERROR</b> (zero). Otherwise, it returns <b>SOCKET_ERROR</b> if the function fails, and you must retrieve the appropriate error code using the 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter points to memory that is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified namespace–provider identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSASYSCALLFAILURE</a></b></dt>
</dl>
</td>
<td width="60%">
 A system call that should never fail has failed.

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



<b>WSCUnInstallNameSpace32</b> is a strictly 32-bit version of <a href="https://msdn.microsoft.com/5267f986-99fc-4e53-9fbb-3850bb9d24cf">WSCUnInstallNameSpace</a>. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

The namespace configuration functions do not affect applications that are already running. Newly installed name-space providers will not be visible to applications nor will the changes in a name-space provider's activation state. Applications launched after the call to 
<b>WSCUnInstallNameSpace32</b> will recognize the changes.

On success, <b>WSCUnInstallNameSpace32</b> will attempt to alert all interested applications that have registered for notification of the change by calling <a href="https://msdn.microsoft.com/abaf367a-8f99-478c-a58c-d57e9f9cd8a1">WSAProviderConfigChange</a>.

The <b>WSCUnInstallNameSpace32</b> function can only be called by a user logged on as a member of the Administrators group. If <b>WSCUnInstallNameSpace32</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>WSANO_RECOVERY</b> is returned in the <i>lpErrno</i> parameter.

For computers running on Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to <b>requireAdministrator</b>. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

The caller of this function must remove any additional files or service provider–specific configuration information that is required to completely uninstall the service provider.




## -see-also




<a href="https://msdn.microsoft.com/abaf367a-8f99-478c-a58c-d57e9f9cd8a1">WSAProviderConfigChange</a>



<a href="https://msdn.microsoft.com/3de74059-dbfb-49b9-830b-7b2f81f8b68c">WSCDeinstallProvider32</a>



<a href="https://msdn.microsoft.com/f46042f6-0b14-4a14-abc1-4e40c34b1599">WSCEnumProtocols32</a>



<a href="https://msdn.microsoft.com/b107fbe6-bbfb-45be-8419-4d85d3c4e80c">WSCInstallNameSpace32</a>



<a href="https://msdn.microsoft.com/5267f986-99fc-4e53-9fbb-3850bb9d24cf">WSCUnInstallNameSpace</a>
 

 

