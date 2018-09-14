---
UID: NF:winuser.EmptyClipboard
title: EmptyClipboard function
author: windows-sdk-content
description: Empties the clipboard and frees handles to data in the clipboard. The function then assigns ownership of the clipboard to the window that currently has the clipboard open.
old-location: dataxchg\emptyclipboard.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\emptyclipboard.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EmptyClipboard, EmptyClipboard function [Data Exchange], _win32_EmptyClipboard, _win32_emptyclipboard_cpp, dataxchg.emptyclipboard, winui._win32_emptyclipboard, winuser/EmptyClipboard
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
 - API-MS-Win-RTCore-NTUser-clipboard-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - api-ms-win-ntuser-ie-clipboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - EmptyClipboard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EmptyClipboard function


## -description


Empties the clipboard and frees handles to data in the clipboard. The function then assigns ownership of the clipboard to the window that currently has the clipboard open. 


## -parameters






## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Before calling <b>EmptyClipboard</b>, an application must open the clipboard by using the <a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a> function. If the application specifies a <b>NULL</b> window handle when opening the clipboard, <b>EmptyClipboard</b> succeeds but sets the clipboard owner to <b>NULL</b>. Note that this causes <a href="https://msdn.microsoft.com/45ca0c04-cf1a-4206-a05f-9957e50be89c">SetClipboardData</a> to fail. 


#### Examples

For an example, see <a href="using_the_clipboard.htm">Copying Information to the Clipboard</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/45ca0c04-cf1a-4206-a05f-9957e50be89c">SetClipboardData</a>



<a href="https://msdn.microsoft.com/9f75b7fb-e9ae-4876-ba99-7db931b9c2ff">WM_DESTROYCLIPBOARD</a>
 

 

