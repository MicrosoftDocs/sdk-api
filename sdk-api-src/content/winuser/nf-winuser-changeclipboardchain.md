---
UID: NF:winuser.ChangeClipboardChain
title: ChangeClipboardChain function
author: windows-sdk-content
description: Removes a specified window from the chain of clipboard viewers.
old-location: dataxchg\changeclipboardchain.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\changeclipboardchain.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: ChangeClipboardChain, ChangeClipboardChain function [Data Exchange], _win32_ChangeClipboardChain, _win32_changeclipboardchain_cpp, dataxchg.changeclipboardchain, winui._win32_changeclipboardchain, winuser/ChangeClipboardChain
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
req.typenames: AR_STATE, *PAR_STATE
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ChangeClipboardChain function


## -description


Removes a specified window from the chain of clipboard viewers.


## -parameters




### -param hWndRemove [in]

Type: <b>HWND</b>

A handle to the window to be removed from the chain. The handle must have been passed to the <a href="https://msdn.microsoft.com/b1c9c0eb-388f-4fa1-9744-8ebd324cec4f">SetClipboardViewer</a> function.


### -param hWndNewNext [in]

Type: <b>HWND</b>

A handle to the window that follows the 
     <i>hWndRemove</i> window in the clipboard viewer chain. (This is the handle returned by <a href="https://msdn.microsoft.com/b1c9c0eb-388f-4fa1-9744-8ebd324cec4f">SetClipboardViewer</a>, unless the sequence was changed in response to a <a href="https://msdn.microsoft.com/7be87342-87fa-4cd2-b066-0b36b7ef52f5">WM_CHANGECBCHAIN</a> message.)


## -returns



Type: <b>BOOL</b>

The return value indicates the result of passing the <a href="https://msdn.microsoft.com/7be87342-87fa-4cd2-b066-0b36b7ef52f5">WM_CHANGECBCHAIN</a> message to the windows in the clipboard viewer chain. Because a window in the chain typically returns <b>FALSE</b> when it processes <b>WM_CHANGECBCHAIN</b>, the return value from <b>ChangeClipboardChain</b> is typically <b>FALSE</b>. If there is only one window in the chain, the return value is typically <b>TRUE</b>.




## -remarks



The window identified by 
    <i>hWndNewNext</i> replaces the 
    <i>hWndRemove</i> window in the chain. The <a href="https://msdn.microsoft.com/b1c9c0eb-388f-4fa1-9744-8ebd324cec4f">SetClipboardViewer</a> function sends a <a href="https://msdn.microsoft.com/7be87342-87fa-4cd2-b066-0b36b7ef52f5">WM_CHANGECBCHAIN</a> message to the first window in the clipboard viewer chain.

For an example, see <a href="using_the_clipboard.htm">Removing a Window from the Clipboard Viewer Chain</a>.




## -see-also




<a href="https://msdn.microsoft.com/438ff6b4-6b45-4163-87bc-2f354c73fced">ChangeClipboardChain</a>



<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b1c9c0eb-388f-4fa1-9744-8ebd324cec4f">SetClipboardViewer</a>



<a href="https://msdn.microsoft.com/7be87342-87fa-4cd2-b066-0b36b7ef52f5">WM_CHANGECBCHAIN</a>
 

 

