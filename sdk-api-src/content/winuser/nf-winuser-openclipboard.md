---
UID: NF:winuser.OpenClipboard
title: OpenClipboard function
author: windows-sdk-content
description: Opens the clipboard for examination and prevents other applications from modifying the clipboard content.
old-location: dataxchg\openclipboard.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\openclipboard.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: OpenClipboard, OpenClipboard function [Data Exchange], _win32_OpenClipboard, _win32_openclipboard_cpp, dataxchg.openclipboard, winui._win32_openclipboard, winuser/OpenClipboard
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
 - OpenClipboard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- OpenClipboard
: 
---

# OpenClipboard function


## -description


Opens the clipboard for examination and prevents other applications from modifying the clipboard content. 


## -parameters




### -param hWndNewOwner [in, optional]

Type: <b>HWND</b>

A handle to the window to be associated with the open clipboard. If this parameter is <b>NULL</b>, the open clipboard is associated with the current task. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>OpenClipboard</b> fails if another window has the clipboard open. 

An application should call the <a href="https://msdn.microsoft.com/en-us/library/ms649035(v=VS.85).aspx">CloseClipboard</a> function after every successful call to <b>OpenClipboard</b>. 

The window identified by the 
				<i>hWndNewOwner</i> parameter does not become the clipboard owner unless the <a href="https://msdn.microsoft.com/en-us/library/ms649037(v=VS.85).aspx">EmptyClipboard</a> function is called. 

If an application calls <b>OpenClipboard</b> with hwnd set to <b>NULL</b>, <a href="https://msdn.microsoft.com/en-us/library/ms649037(v=VS.85).aspx">EmptyClipboard</a> sets the clipboard owner to <b>NULL</b>; this causes <a href="https://msdn.microsoft.com/en-us/library/ms649051(v=VS.85).aspx">SetClipboardData</a> to fail.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms649016(v=VS.85).aspx">Copying Information to the Clipboard</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648709(v=VS.85).aspx">Clipboard</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649035(v=VS.85).aspx">CloseClipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649037(v=VS.85).aspx">EmptyClipboard</a>



<b>Reference</b>
 

 

