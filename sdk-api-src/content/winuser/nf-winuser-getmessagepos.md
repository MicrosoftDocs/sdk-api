---
UID: NF:winuser.GetMessagePos
title: GetMessagePos function
author: windows-sdk-content
description: Retrieves the cursor position for the last message retrieved by the GetMessage function.
old-location: winmsg\getmessagepos.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getmessagepos.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMessagePos, GetMessagePos function [Windows and Messages], _win32_GetMessagePos, _win32_getmessagepos_cpp, winmsg.getmessagepos, winui._win32_getmessagepos, winuser/GetMessagePos
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-message-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - GetMessagePos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMessagePos function


## -description


Retrieves the cursor position for the last message retrieved by the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> function.

			

To determine the current position of the cursor, use the <a href="https://msdn.microsoft.com/c76370d3-741a-4192-97d4-d63d2885b36b">GetCursorPos</a> function.


## -parameters






## -returns



Type: <strong>Type: <b>DWORD</b>
</strong>

The return value specifies the x- and y-coordinates of the cursor position. The x-coordinate is the low order <b>short</b> and the y-coordinate is the high-order <b>short</b>.




## -remarks



As noted above, the x-coordinate is in the low-order <b>short</b> of the return value; the y-coordinate is in the high-order <b>short</b> (both represent <i>signed</i> values because they can take negative values on systems with multiple monitors). If the return value is assigned to a variable, you can use the <a href="https://msdn.microsoft.com/1f84cfd0-2836-4c20-9408-17e0d57742be">MAKEPOINTS</a> macro to obtain a <a href="https://msdn.microsoft.com/d36bc846-c538-4a37-bb5d-c75d41a3c7cc">POINTS</a> structure from the return value. You can also use the <a href="https://msdn.microsoft.com/40f7dde6-1486-4050-b9b6-ffc2ed9982a9">GET_X_LPARAM</a> or <a href="https://msdn.microsoft.com/eaf1b26d-14e7-45e9-bdd1-79258c5f9701">GET_Y_LPARAM</a> macro to extract the x- or y-coordinate. 

<div class="alert"><b>Important</b>  Do not use the <a href="https://msdn.microsoft.com/4f169f33-ed13-4efc-bf3f-ea2a4fe1de4e">LOWORD</a> or <a href="https://msdn.microsoft.com/9f79d489-ff3f-437c-821e-fd353d712c7b">HIWORD</a> macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors. Systems with multiple monitors can have negative x- and y- coordinates, and <b>LOWORD</b> and <b>HIWORD</b> treat the coordinates as unsigned quantities.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/c76370d3-741a-4192-97d4-d63d2885b36b">GetCursorPos</a>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/e65edd3d-e64e-41a6-bf38-d79663b673e9">GetMessageTime</a>



<a href="https://msdn.microsoft.com/9f79d489-ff3f-437c-821e-fd353d712c7b">HIWORD</a>



<a href="https://msdn.microsoft.com/4f169f33-ed13-4efc-bf3f-ea2a4fe1de4e">LOWORD</a>



<a href="https://msdn.microsoft.com/1f84cfd0-2836-4c20-9408-17e0d57742be">MAKEPOINTS</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/d36bc846-c538-4a37-bb5d-c75d41a3c7cc">POINTS</a>



<b>Reference</b>
 

 

