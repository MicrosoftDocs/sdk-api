---
UID: NF:winuser.IsClipboardFormatAvailable
title: IsClipboardFormatAvailable function
author: windows-sdk-content
description: Determines whether the clipboard contains data in the specified format.
old-location: dataxchg\isclipboardformatavailable.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\isclipboardformatavailable.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IsClipboardFormatAvailable, IsClipboardFormatAvailable function [Data Exchange], _win32_IsClipboardFormatAvailable, _win32_isclipboardformatavailable_cpp, dataxchg.isclipboardformatavailable, winui._win32_isclipboardformatavailable, winuser/IsClipboardFormatAvailable
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
 - IsClipboardFormatAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



Typically, an application that recognizes only one clipboard format would call this function when processing the <a href="https://msdn.microsoft.com/en-us/library/ms646344(v=VS.85).aspx">WM_INITMENU</a> or <a href="https://msdn.microsoft.com/en-us/library/ms646347(v=VS.85).aspx">WM_INITMENUPOPUP</a> message. The application would then enable or disable the Paste menu item, depending on the return value. Applications that recognize more than one clipboard format should use the <a href="https://msdn.microsoft.com/en-us/library/ms649045(v=VS.85).aspx">GetPriorityClipboardFormat</a> function for this purpose. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms649016(v=VS.85).aspx">Pasting Information from the Clipboard</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648709(v=VS.85).aspx">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649036(v=VS.85).aspx">CountClipboardFormats</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649038(v=VS.85).aspx">EnumClipboardFormats</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649045(v=VS.85).aspx">GetPriorityClipboardFormat</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649049(v=VS.85).aspx">RegisterClipboardFormat</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646344(v=VS.85).aspx">WM_INITMENU</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646347(v=VS.85).aspx">WM_INITMENUPOPUP</a>
 

 

