---
UID: NF:ws2spi.WPUResetEvent
title: WPUResetEvent function
author: windows-sdk-content
description: The WPUResetEvent function resets the state of the specified event object to nonsignaled. This call is safe for use within interrupt context.
old-location: winsock\wpuresetevent_2.htm
old-project: WinSock
ms.assetid: a3385c77-899c-4772-88b9-fb3e0fab54e0
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: WPUResetEvent, WPUResetEvent function [Winsock], _win32_wpuresetevent_2, winsock.wpuresetevent_2, ws2spi/WPUResetEvent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSC_PROVIDER_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ws2spi.h
api_name:
-	WPUResetEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WPUResetEvent function


## -description



			The 
<b>WPUResetEvent</b> function resets the state of the specified event object to nonsignaled. This call is safe for use within interrupt context.


## -parameters




### -param hEvent [in]

Handle that identifies an open event object.


### -param lpErrno [out]

Pointer to the error code.


## -returns




						If no error occurs, the 
<b>WPUResetEvent</b> function returns the value <b>TRUE</b>. Otherwise, <b>FALSE</b> is returned, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> parameter is not a valid event object handle.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/d8c6133b-e5a7-4936-a796-0930bb95fd0c">WPUCloseEvent</a>



<a href="https://msdn.microsoft.com/61e71e93-e35f-4122-bd4d-c103f652d2ca">WPUCreateEvent</a>



<a href="https://msdn.microsoft.com/d5caa926-1223-4917-85ba-4f79731e955a">WPUSetEvent</a>
 

 

