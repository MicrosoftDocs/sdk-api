---
UID: NF:ws2spi.WSCEnableNSProvider32
title: WSCEnableNSProvider32 function
author: windows-sdk-content
description: Enables or disables a specified 32-bit namespace provider.
old-location: winsock\wscenablensprovider32.htm
tech.root: winsock
ms.assetid: 5ab4f8bd-d32d-4962-aac7-2d92847d0e03
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WSCEnableNSProvider32, WSCEnableNSProvider32 function [Winsock], winsock.wscenablensprovider32, ws2spi/WSCEnableNSProvider32
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WSCEnableNSProvider32
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSCEnableNSProvider32 function


## -description


The <b>WSCEnableNSProvider32</b> function enables or disables a specified 32-bit namespace provider. It is intended to give the end-user the ability to change the state of the namespace providers.<div class="alert"><b>Note</b>  This call is a strictly 32-bit version of <a href="https://msdn.microsoft.com/2dff5af6-3011-4e3f-b812-fffaca8fa2d9">WSCEnableNSProvider</a> for use on 64-bit computers. It is provided to allow 64-bit processes to access the 32-bit catalogs.</div>
<div> </div>



## -parameters




### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the namespace provider.


### -param fEnable [in]

A Boolean value that, if <b>TRUE</b>, the namespace provider is set to the active state. If <b>FALSE</b>, the namespace provider is disabled and will not be available for query operations or service registration.


## -returns



If no error occurs, the 
<b>WSCEnableNSProvider32</b> function returns <b>NO_ERROR</b> (zero). Otherwise, it returns <b>SOCKET_ERROR</b> if the function fails, and you must retrieve the appropriate error code using the 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function.

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
The <i>lpProviderId</i> parameter points to memory that is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified namespace provider identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSASYSCALLFAILURE</a></b></dt>
</dl>
</td>
<td width="60%">
 A system call that should never fail has failed.

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
<b>WSCEnableNSProvider32</b> function is intended to be used to change the state of the namespace providers. An independent software vendor (ISV) should not normally de-activate another ISV's namespace provider in order to activate its own. The choice should be left to the user.    

<b>WSCEnableNSProvider32</b> is a strictly 32-bit version of <a href="https://msdn.microsoft.com/2dff5af6-3011-4e3f-b812-fffaca8fa2d9">WSCEnableNSProvider</a>. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

The namespace configuration functions do not affect applications that are already running. Newly installed namespace providers will not be visible to applications nor will the changes in a namespace provider's activation state. Applications launched after the call to 
<b>WSCEnableNSProvider32</b> will see the changes.

The <b>WSCEnableNSProvider32</b> function can only be called by a user logged on as a member of the Administrators group. If <b>WSCEnableNSProvider32</b> is called by a user that is not a member of the Administrators group, the function call will fail.

For computers running on Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to <b>requireAdministrator</b>. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.




## -see-also




<a href="https://msdn.microsoft.com/2dff5af6-3011-4e3f-b812-fffaca8fa2d9">WSCEnableNSProvider</a>



<a href="https://msdn.microsoft.com/f46042f6-0b14-4a14-abc1-4e40c34b1599">WSCEnumProtocols32</a>



<a href="https://msdn.microsoft.com/b107fbe6-bbfb-45be-8419-4d85d3c4e80c">WSCInstallNameSpace32</a>



<a href="https://msdn.microsoft.com/a2a08159-6ac0-493d-8f9f-d19aa199a65f">WSCUnInstallNameSpace32</a>



<a href="https://msdn.microsoft.com/a5b15d28-8137-42bf-8f2a-7c6b5a8a63c2">WSCWriteNameSpaceOrder32</a>
 

 

