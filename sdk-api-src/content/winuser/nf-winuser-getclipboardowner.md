---
UID: NF:winuser.GetClipboardOwner
title: GetClipboardOwner function
author: windows-sdk-content
description: Retrieves the window handle of the current owner of the clipboard.
old-location: dataxchg\getclipboardowner.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getclipboardowner.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: GetClipboardOwner, GetClipboardOwner function [Data Exchange], _win32_GetClipboardOwner, _win32_getclipboardowner_cpp, dataxchg.getclipboardowner, winui._win32_getclipboardowner, winuser/GetClipboardOwner
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
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetClipboardOwner
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetClipboardOwner function


## -description


Retrieves the window handle of the current owner of the clipboard. 


## -parameters






## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the window that owns the clipboard. 

If the clipboard is not owned, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The clipboard can still contain data even if the clipboard is not currently owned. 

In general, the clipboard owner is the window that last placed data in clipboard. The <a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a> function assigns clipboard ownership. 


#### Examples

For an example, see <a href="using_the_clipboard.htm">Example of a Clipboard Viewer</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a>



<a href="https://msdn.microsoft.com/700bee1f-1bed-4fc8-a4ce-7a48bd05e90b">GetClipboardViewer</a>



<b>Reference</b>
 

 

