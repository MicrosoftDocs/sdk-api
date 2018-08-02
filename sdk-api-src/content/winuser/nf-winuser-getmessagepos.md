---
UID: NF:winuser.GetMessagePos
title: GetMessagePos function
author: windows-sdk-content
description: Retrieves the cursor position for the last message retrieved by the GetMessage function.
old-location: winmsg\getmessagepos.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\getmessagepos.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetMessagePos, GetMessagePos function [Windows and Messages], _win32_GetMessagePos, _win32_getmessagepos_cpp, winmsg.getmessagepos, winui._win32_getmessagepos, winuser/GetMessagePos
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetMessagePos function


## -description


Retrieves the cursor position for the last message retrieved by the <a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a> function.

			

To determine the current position of the cursor, use the <a href="https://msdn.microsoft.com/en-us/library/ms648390(v=VS.85).aspx">GetCursorPos</a> function.


## -parameters






## -returns



Type: <strong>Type: <b>DWORD</b>
</strong>

The return value specifies the x- and y-coordinates of the cursor position. The x-coordinate is the low order <b>short</b> and the y-coordinate is the high-order <b>short</b>.




## -remarks



As noted above, the x-coordinate is in the low-order <b>short</b> of the return value; the y-coordinate is in the high-order <b>short</b> (both represent <i>signed</i> values because they can take negative values on systems with multiple monitors). If the return value is assigned to a variable, you can use the <a href="https://msdn.microsoft.com/1f84cfd0-2836-4c20-9408-17e0d57742be">MAKEPOINTS</a> macro to obtain a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569167">POINTS</a> structure from the return value. You can also use the <a href="https://msdn.microsoft.com/en-us/library/ms632654(v=VS.85).aspx">GET_X_LPARAM</a> or <a href="https://msdn.microsoft.com/en-us/library/ms632655(v=VS.85).aspx">GET_Y_LPARAM</a> macro to extract the x- or y-coordinate. 

<div class="alert"><b>Important</b>  Do not use the <a href="https://msdn.microsoft.com/en-us/library/ms632659(v=VS.85).aspx">LOWORD</a> or <a href="https://msdn.microsoft.com/en-us/library/ms632657(v=VS.85).aspx">HIWORD</a> macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors. Systems with multiple monitors can have negative x- and y- coordinates, and <b>LOWORD</b> and <b>HIWORD</b> treat the coordinates as unsigned quantities.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648390(v=VS.85).aspx">GetCursorPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644939(v=VS.85).aspx">GetMessageTime</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632657(v=VS.85).aspx">HIWORD</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632659(v=VS.85).aspx">LOWORD</a>



<a href="https://msdn.microsoft.com/1f84cfd0-2836-4c20-9408-17e0d57742be">MAKEPOINTS</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569167">POINTS</a>



<b>Reference</b>
 

 

