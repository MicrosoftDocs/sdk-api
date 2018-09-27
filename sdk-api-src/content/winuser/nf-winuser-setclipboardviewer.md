---
UID: NF:winuser.SetClipboardViewer
title: SetClipboardViewer function
author: windows-sdk-content
description: Adds the specified window to the chain of clipboard viewers. Clipboard viewer windows receive a WM_DRAWCLIPBOARD message whenever the content of the clipboard changes. This function is used for backward compatibility with earlier versions of Windows.
old-location: dataxchg\setclipboardviewer.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\setclipboardviewer.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetClipboardViewer, SetClipboardViewer function [Data Exchange], _win32_SetClipboardViewer, _win32_setclipboardviewer_cpp, dataxchg.setclipboardviewer, winui._win32_setclipboardviewer, winuser/SetClipboardViewer
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
 - SetClipboardViewer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClipboardViewer function


## -description


Adds the specified window to the chain of clipboard viewers. Clipboard viewer windows receive a <a href="https://msdn.microsoft.com/en-us/library/ms649025(v=VS.85).aspx">WM_DRAWCLIPBOARD</a> message whenever the content of the clipboard changes. This function is used for backward compatibility with earlier versions of Windows.


## -parameters




### -param hWndNewViewer [in]

Type: <b>HWND</b>

A handle to the window to be added to the clipboard chain.


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value identifies the next window in the clipboard viewer chain. If an error occurs or there are no other windows in the clipboard viewer chain, the return value is NULL. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The windows that are part of the clipboard viewer chain, called clipboard viewer windows, must process the clipboard messages <a href="https://msdn.microsoft.com/en-us/library/ms649019(v=VS.85).aspx">WM_CHANGECBCHAIN</a> and <a href="https://msdn.microsoft.com/en-us/library/ms649025(v=VS.85).aspx">WM_DRAWCLIPBOARD</a>. Each clipboard viewer window calls the <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a> function to pass these messages to the next window in the clipboard viewer chain.

A clipboard viewer window must eventually remove itself from the clipboard viewer chain by calling the <a href="https://msdn.microsoft.com/en-us/library/ms649034(v=VS.85).aspx">ChangeClipboardChain</a> function — for example, in response to the <a href="https://msdn.microsoft.com/en-us/library/ms632620(v=VS.85).aspx">WM_DESTROY</a> message.

The <b>SetClipboardViewer</b> function exists to provide backward compatibility with earlier versions of Windows. The clipboard viewer chain can be broken by an application that fails to handle the clipboard chain messages properly. New applications should use more robust techniques such as the clipboard sequence number or the registration of a clipboard format listener. For further details on these alternatives techniques, see <a href="https://msdn.microsoft.com/en-us/library/ms649016(v=VS.85).aspx">Monitoring Clipboard Contents</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms649016(v=VS.85).aspx">Adding a Window to the Clipboard Viewer Chain</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649034(v=VS.85).aspx">ChangeClipboardChain</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648709(v=VS.85).aspx">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649043(v=VS.85).aspx">GetClipboardViewer</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a>
 

 

