---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

