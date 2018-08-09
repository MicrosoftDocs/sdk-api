---
UID: NF:winuser.IsClipboardFormatAvailable
title: IsClipboardFormatAvailable function
author: windows-sdk-content
description: Determines whether the clipboard contains data in the specified format.
old-location: dataxchg\isclipboardformatavailable.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\isclipboardformatavailable.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IsClipboardFormatAvailable, IsClipboardFormatAvailable function [Data Exchange], _win32_IsClipboardFormatAvailable, _win32_isclipboardformatavailable_cpp, dataxchg.isclipboardformatavailable, winui._win32_isclipboardformatavailable, winuser/IsClipboardFormatAvailable
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
req.typenames: 
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
 - IsClipboardFormatAvailable
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IsClipboardFormatAvailable function


## -description


Determines whether the clipboard contains data in the specified format. 


## -parameters




### -param format [in]

Type: <b>UINT</b>

A standard or registered clipboard format. For a description of the standard clipboard formats, see <a href="https://msdn.microsoft.com/f0af4e61-7ef1-4263-b2c5-e4114515124f">Standard Clipboard Formats</a> . 


## -returns



Type: <b>BOOL</b>

If the clipboard format is available, the return value is nonzero.

If the clipboard format is not available, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Typically, an application that recognizes only one clipboard format would call this function when processing the <a href="https://msdn.microsoft.com/d0fcc6d8-f57c-4d04-b9e7-4cfab6add173">WM_INITMENU</a> or <a href="https://msdn.microsoft.com/08ae1a78-5e68-488c-9b77-ee42044ca3ab">WM_INITMENUPOPUP</a> message. The application would then enable or disable the Paste menu item, depending on the return value. Applications that recognize more than one clipboard format should use the <a href="https://msdn.microsoft.com/7ece4b0e-2374-4b49-b4e9-278c3317f935">GetPriorityClipboardFormat</a> function for this purpose. 


#### Examples

For an example, see <a href="using_the_clipboard.htm">Pasting Information from the Clipboard</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3f9390f0-0fcb-4654-add0-eeea8f79b3f5">CountClipboardFormats</a>



<a href="https://msdn.microsoft.com/eca6e3ca-46d1-4f1d-a13c-63542e8eb8bf">EnumClipboardFormats</a>



<a href="https://msdn.microsoft.com/7ece4b0e-2374-4b49-b4e9-278c3317f935">GetPriorityClipboardFormat</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/892add91-a937-4602-86d2-5e5550a81872">RegisterClipboardFormat</a>



<a href="https://msdn.microsoft.com/d0fcc6d8-f57c-4d04-b9e7-4cfab6add173">WM_INITMENU</a>



<a href="https://msdn.microsoft.com/08ae1a78-5e68-488c-9b77-ee42044ca3ab">WM_INITMENUPOPUP</a>
 

 

