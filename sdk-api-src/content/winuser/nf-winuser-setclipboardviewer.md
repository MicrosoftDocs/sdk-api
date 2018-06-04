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

# SetClipboardViewer function


## -description


Adds the specified window to the chain of clipboard viewers. Clipboard viewer windows receive a <a href="https://msdn.microsoft.com/ffaadf6f-588b-4a29-b26c-629087e7ce73">WM_DRAWCLIPBOARD</a> message whenever the content of the clipboard changes. This function is used for backward compatibility with earlier versions of Windows.


## -parameters




### -param hWndNewViewer [in]

Type: <b>HWND</b>

A handle to the window to be added to the clipboard chain.


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value identifies the next window in the clipboard viewer chain. If an error occurs or there are no other windows in the clipboard viewer chain, the return value is NULL. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The windows that are part of the clipboard viewer chain, called clipboard viewer windows, must process the clipboard messages <a href="https://msdn.microsoft.com/7be87342-87fa-4cd2-b066-0b36b7ef52f5">WM_CHANGECBCHAIN</a> and <a href="https://msdn.microsoft.com/ffaadf6f-588b-4a29-b26c-629087e7ce73">WM_DRAWCLIPBOARD</a>. Each clipboard viewer window calls the <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a> function to pass these messages to the next window in the clipboard viewer chain.

A clipboard viewer window must eventually remove itself from the clipboard viewer chain by calling the <a href="https://msdn.microsoft.com/438ff6b4-6b45-4163-87bc-2f354c73fced">ChangeClipboardChain</a> function — for example, in response to the <a href="https://msdn.microsoft.com/089c0645-199b-4a90-9cbc-740f0cf3267d">WM_DESTROY</a> message.

The <b>SetClipboardViewer</b> function exists to provide backward compatibility with earlier versions of Windows. The clipboard viewer chain can be broken by an application that fails to handle the clipboard chain messages properly. New applications should use more robust techniques such as the clipboard sequence number or the registration of a clipboard format listener. For further details on these alternatives techniques, see <a href="using_the_clipboard.htm">Monitoring Clipboard Contents</a>.


#### Examples

For an example, see <a href="using_the_clipboard.htm">Adding a Window to the Clipboard Viewer Chain</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/438ff6b4-6b45-4163-87bc-2f354c73fced">ChangeClipboardChain</a>



<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/700bee1f-1bed-4fc8-a4ce-7a48bd05e90b">GetClipboardViewer</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>
 

 

