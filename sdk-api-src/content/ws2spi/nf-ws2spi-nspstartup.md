---
UID: NF:ws2spi.NSPStartup
title: NSPStartup function
author: windows-sdk-content
description: Retrieves the dynamic information about a provider, such as the list of the DLL entry points.
old-location: winsock\nspstartup_2.htm
tech.root: winsock
ms.assetid: ed9e4ff3-736a-4037-bf85-5572f0cd279d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: NSPStartup, NSPStartup function [Winsock], _win32_nspstartup_2, winsock.nspstartup_2, ws2spi/NSPStartup
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPStartup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NSPStartup function


## -description


The 
<b>NSPStartup</b> function retrieves the dynamic information about a provider, such as the list of the DLL entry points.

This function is called by the client upon initialization. 
The <b>NSPStartup</b> and 
<a href="https://msdn.microsoft.com/bef888a2-7cfd-4096-bd03-e1864af42365">NSPCleanup</a> functions must be called as pairs. All  NSP functions must be called from within an <b>NSPStartup</b>/<b>NSPCleanup</b> pair. It is not required that WSC functions be called from within a <b>NSPStartup</b>/<b>NSPCleanup</b> pair.


## -parameters




### -param lpProviderId [in]

The desired provider from which to return the entry points.


### -param lpnspRoutines [out]

A pointer to an <a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a> structure that points to provider entry points if the function call is successful.


## -returns



The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (–1) if the function fails and it must set the appropriate error code using 
<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more parameters were invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVALIDPROCTABLE</a></b></dt>
</dl>
</td>
<td width="60%">
The procedure call table is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSASYSNOTREADY</a></b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/ed9e4ff3-736a-4037-bf85-5572f0cd279d">NSPStartup</a> function cannot operate at this time because the underlying system it uses to provide network services is currently unavailable.

</td>
</tr>
</table>
 




## -remarks



For more information, see the <a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/bef888a2-7cfd-4096-bd03-e1864af42365">NSPCleanup</a>



<a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

