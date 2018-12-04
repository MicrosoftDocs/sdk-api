---
UID: NF:winuser.CloseClipboard
title: CloseClipboard function
author: windows-sdk-content
description: Closes the clipboard.
old-location: dataxchg\closeclipboard.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\closeclipboard.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CloseClipboard, CloseClipboard function [Data Exchange], _win32_CloseClipboard, _win32_closeclipboard_cpp, dataxchg.closeclipboard, winui._win32_closeclipboard, winuser/CloseClipboard
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
 - CloseClipboard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseClipboard function


## -description


Closes the clipboard. 


## -parameters






## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



When the window has finished examining or changing the clipboard, close the clipboard by calling <b>CloseClipboard</b>. This enables other windows to access the clipboard.

Do not place an object on the clipboard after calling <b>CloseClipboard</b>. 


#### Examples

For an example, see <a href="using_the_clipboard.htm">Example of a Clipboard Viewer</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d90f8734-a23e-4092-a387-ac2f31443395">GetOpenClipboardWindow</a>



<a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a>



<b>Reference</b>
 

 

