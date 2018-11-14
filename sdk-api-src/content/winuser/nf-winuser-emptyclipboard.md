---
UID: NF:winuser.EmptyClipboard
title: EmptyClipboard function
author: windows-sdk-content
description: Empties the clipboard and frees handles to data in the clipboard. The function then assigns ownership of the clipboard to the window that currently has the clipboard open.
old-location: dataxchg\emptyclipboard.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\emptyclipboard.htm
ms.author: windowssdkdev
ms.date: 11/13/2018
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
- apiref
: 
- 
: 
- EmptyClipboard
: 
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



Before calling <b>EmptyClipboard</b>, an application must open the clipboard by using the <a href="https://msdn.microsoft.com/en-us/library/ms649048(v=VS.85).aspx">OpenClipboard</a> function. If the application specifies a <b>NULL</b> window handle when opening the clipboard, <b>EmptyClipboard</b> succeeds but sets the clipboard owner to <b>NULL</b>. Note that this causes <a href="https://msdn.microsoft.com/en-us/library/ms649051(v=VS.85).aspx">SetClipboardData</a> to fail. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms649016(v=VS.85).aspx">Copying Information to the Clipboard</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648709(v=VS.85).aspx">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649048(v=VS.85).aspx">OpenClipboard</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649051(v=VS.85).aspx">SetClipboardData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649024(v=VS.85).aspx">WM_DESTROYCLIPBOARD</a>
 

 

