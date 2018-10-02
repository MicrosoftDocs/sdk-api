---
UID: NF:winuser.SetClipboardData
title: SetClipboardData function
author: windows-sdk-content
description: Places data on the clipboard in a specified clipboard format.
old-location: dataxchg\setclipboarddata.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\setclipboarddata.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetClipboardData, SetClipboardData function [Data Exchange], _win32_SetClipboardData, _win32_setclipboarddata_cpp, dataxchg.setclipboarddata, winui._win32_setclipboarddata, winuser/SetClipboardData
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
 - SetClipboardData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClipboardData function


## -description


Places data on the clipboard in a specified clipboard format. The window must be the current clipboard owner, and the application must have called the <a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a> function. (When responding to the <a href="https://msdn.microsoft.com/81638109-4c5e-4b4c-b2db-4208b6ee83cc">WM_RENDERFORMAT</a> and <a href="https://msdn.microsoft.com/dff9100f-2dba-467d-be74-a9a9c2b2122b">WM_RENDERALLFORMATS</a> messages, the clipboard owner must not call <b>OpenClipboard</b> before calling <b>SetClipboardData</b>.)


## -parameters




### -param uFormat [in]

Type: <b>UINT</b>

The clipboard format. This parameter can be a registered format or any of the standard clipboard formats. For more information, see <a href="https://msdn.microsoft.com/f0af4e61-7ef1-4263-b2c5-e4114515124f">Standard Clipboard Formats</a> and <a href="clipboard_formats.htm">Registered Clipboard Formats</a>.


### -param hMem [in, optional]

Type: <b>HANDLE</b>

A handle to the data in the specified format. This parameter can be <b>NULL</b>, indicating that the window provides data in the specified clipboard format (renders the format) upon request. If a window delays rendering, it must process the <a href="https://msdn.microsoft.com/81638109-4c5e-4b4c-b2db-4208b6ee83cc">WM_RENDERFORMAT</a> and <a href="https://msdn.microsoft.com/dff9100f-2dba-467d-be74-a9a9c2b2122b">WM_RENDERALLFORMATS</a> messages.

If <b>SetClipboardData</b> succeeds, the system owns the object identified by the <i>hMem</i> parameter. The application may not write to or free the data once ownership has been transferred to the system, but it can lock and read from the data until the <a href="https://msdn.microsoft.com/34658e02-cbac-4e5a-afb3-a1450274b5b1">CloseClipboard</a> function is called. (The memory must be unlocked before the Clipboard is closed.) If the <i>hMem</i> parameter identifies a memory object, the object must have been allocated using the function with the <b>GMEM_MOVEABLE</b> flag.


## -returns



Type: <b>HANDLE</b>

If the function succeeds, the return value is the handle to the data.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>Windows 8:</b> Bitmaps to be shared with Windows Store app apps must be in the <b>CF_BITMAP</b> format (device-dependent bitmap). 

If an application calls <b>SetClipboardData</b> in response to <a href="https://msdn.microsoft.com/81638109-4c5e-4b4c-b2db-4208b6ee83cc">WM_RENDERFORMAT</a> or <a href="https://msdn.microsoft.com/dff9100f-2dba-467d-be74-a9a9c2b2122b">WM_RENDERALLFORMATS</a>, the application should not use the handle after <b>SetClipboardData</b> has been called.

If an application calls <a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a> with hwnd set to <b>NULL</b>, <a href="https://msdn.microsoft.com/3b0c1f36-eebe-4f69-887e-c9ceb947a94e">EmptyClipboard</a> sets the clipboard owner to <b>NULL</b>; this causes <b>SetClipboardData</b> to fail.

The system performs implicit data format conversions between certain clipboard formats when an application calls the <a href="https://msdn.microsoft.com/5c2adab4-1e13-41a6-9ab9-6ae8a2a2d9f3">GetClipboardData</a> function. For example, if the <b>CF_OEMTEXT</b> format is on the clipboard, a window can retrieve data in the <b>CF_TEXT</b> format. The format on the clipboard is converted to the requested format on demand. For more information, see <a href="clipboard_formats.htm">Synthesized Clipboard Formats</a>.


#### Examples

For an example, see <a href="using_the_clipboard.htm">Copying Information to the Clipboard</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<a href="https://msdn.microsoft.com/34658e02-cbac-4e5a-afb3-a1450274b5b1">CloseClipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5c2adab4-1e13-41a6-9ab9-6ae8a2a2d9f3">GetClipboardData</a>



<a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/892add91-a937-4602-86d2-5e5550a81872">RegisterClipboardFormat</a>



<a href="https://msdn.microsoft.com/dff9100f-2dba-467d-be74-a9a9c2b2122b">WM_RENDERALLFORMATS</a>



<a href="https://msdn.microsoft.com/81638109-4c5e-4b4c-b2db-4208b6ee83cc">WM_RENDERFORMAT</a>
 

 

