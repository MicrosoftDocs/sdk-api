---
UID: NC:winfax.PFAXCLOSE
title: PFAXCLOSE
author: windows-sdk-content
description: The FaxClose function closes the following types of fax handles:
old-location: fax\_mfax_faxclose.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5h2d.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: FaxCloseA, FaxCloseW, PFAXCLOSE, PFAXCLOSE callback, PFAXCLOSE callback function [Fax Service], _mfax_faxclose, fax._mfax_faxclose, winfax/FaxCloseA, winfax/FaxCloseW, winfax/PFAXCLOSE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxCloseW (Unicode) and FaxCloseA (ANSI)
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
 - Winfax.h
api_name:
 - PFAXCLOSE
 - FaxCloseA
 - FaxCloseW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFAXCLOSE callback function


## -description


The <b>FaxClose</b> function closes the following types of fax handles:


<ul>
<li>A fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function</li>
<li>A fax port handle returned by a call to the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function</li>
</ul>



## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies the fax handle to close. This value can be a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function, or a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_PORT_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



A fax client application must call the <b>FaxClose</b> function as the last function before it terminates. The <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function cannot close the handle to a fax server or a fax port.

When the <b>FaxClose</b> function closes a handle allocated by the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function, the function disconnects the calling application from the specified fax server.

A fax client application continues to receive fax events from the fax service after the application successfully calls the <b>FaxClose</b> function to close a fax server handle. This permits the fax service to shut down and conserve system resources when the service has been idle for an extended period. If you keep the handle to the fax server open, the fax service does not shut down.

For more information, see <a href="https://msdn.microsoft.com/f226b757-af51-4161-95d5-1c73bf1ccbef">Enabling an Application to Receive Notifications of Fax Events</a>, <a href="https://msdn.microsoft.com/da213475-2cfb-4524-80af-51c1ee0bf658">Connecting to a Fax Server</a> and <a href="https://msdn.microsoft.com/02d276b7-bcbc-4bbe-8051-d9b35f12dc93">Disconnecting from a Fax Server</a>, and <a href="https://msdn.microsoft.com/921007cf-a836-4e90-a544-b320eea2bd54">FaxInitializeEventQueue</a>.




## -see-also




<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a>
 

 

