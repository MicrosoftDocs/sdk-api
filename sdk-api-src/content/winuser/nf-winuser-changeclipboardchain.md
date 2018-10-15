---
UID: NF:winuser.ChangeClipboardChain
title: ChangeClipboardChain function
author: windows-sdk-content
description: Removes a specified window from the chain of clipboard viewers.
old-location: dataxchg\changeclipboardchain.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\changeclipboardchain.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ChangeClipboardChain, ChangeClipboardChain function [Data Exchange], _win32_ChangeClipboardChain, _win32_changeclipboardchain_cpp, dataxchg.changeclipboardchain, winui._win32_changeclipboardchain, winuser/ChangeClipboardChain
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
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - ChangeClipboardChain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ChangeClipboardChain function


## -description


Removes a specified window from the chain of clipboard viewers.


## -parameters




### -param hWndRemove [in]

Type: <b>HWND</b>

A handle to the window to be removed from the chain. The handle must have been passed to the <a href="https://msdn.microsoft.com/en-us/library/ms649052(v=VS.85).aspx">SetClipboardViewer</a> function.


### -param hWndNewNext [in]

Type: <b>HWND</b>

A handle to the window that follows the 
     <i>hWndRemove</i> window in the clipboard viewer chain. (This is the handle returned by <a href="https://msdn.microsoft.com/en-us/library/ms649052(v=VS.85).aspx">SetClipboardViewer</a>, unless the sequence was changed in response to a <a href="https://msdn.microsoft.com/en-us/library/ms649019(v=VS.85).aspx">WM_CHANGECBCHAIN</a> message.)


## -returns



Type: <b>BOOL</b>

The return value indicates the result of passing the <a href="https://msdn.microsoft.com/en-us/library/ms649019(v=VS.85).aspx">WM_CHANGECBCHAIN</a> message to the windows in the clipboard viewer chain. Because a window in the chain typically returns <b>FALSE</b> when it processes <b>WM_CHANGECBCHAIN</b>, the return value from <b>ChangeClipboardChain</b> is typically <b>FALSE</b>. If there is only one window in the chain, the return value is typically <b>TRUE</b>.




## -remarks



The window identified by 
    <i>hWndNewNext</i> replaces the 
    <i>hWndRemove</i> window in the chain. The <a href="https://msdn.microsoft.com/en-us/library/ms649052(v=VS.85).aspx">SetClipboardViewer</a> function sends a <a href="https://msdn.microsoft.com/en-us/library/ms649019(v=VS.85).aspx">WM_CHANGECBCHAIN</a> message to the first window in the clipboard viewer chain.

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms649016(v=VS.85).aspx">Removing a Window from the Clipboard Viewer Chain</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649034(v=VS.85).aspx">ChangeClipboardChain</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648709(v=VS.85).aspx">Clipboard</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649052(v=VS.85).aspx">SetClipboardViewer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649019(v=VS.85).aspx">WM_CHANGECBCHAIN</a>
 

 

