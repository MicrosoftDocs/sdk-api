---
UID: NF:winuser.EnumClipboardFormats
title: EnumClipboardFormats function
author: windows-sdk-content
description: Enumerates the data formats currently available on the clipboard.
old-location: dataxchg\enumclipboardformats.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\enumclipboardformats.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumClipboardFormats, EnumClipboardFormats function [Data Exchange], _win32_EnumClipboardFormats, _win32_enumclipboardformats_cpp, dataxchg.enumclipboardformats, winui._win32_enumclipboardformats, winuser/EnumClipboardFormats
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
api_name:
 - EnumClipboardFormats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumClipboardFormats function


## -description


Enumerates the data formats currently available on the clipboard.

Clipboard data formats are stored in an ordered list. To perform an enumeration of clipboard data formats, you make a series of calls to the <b>EnumClipboardFormats</b> function. For each call, the <i>format</i> parameter specifies an available clipboard format, and the function returns the next available clipboard format. 


## -parameters




### -param format [in]

Type: <b>UINT</b>

A clipboard format that is known to be available.

To start an enumeration of clipboard formats, set 
					<i>format</i> to zero. When 
					<i>format</i> is zero, the function retrieves the first available clipboard format. For subsequent calls during an enumeration, set 
					<i>format</i> to the result of the previous 
					<b>EnumClipboardFormats</b> call. 


## -returns



Type: <b>UINT</b>

If the function succeeds, the return value is the clipboard format that follows the specified format, namely the next available clipboard format.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the clipboard is not open, the function fails. 

If there are no more clipboard formats to enumerate, the return value is zero. In this case, the 
						<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns the value <b>ERROR_SUCCESS</b>. This lets you distinguish between function failure and the end of enumeration.




## -remarks



You must open the clipboard before enumerating its formats. Use the <a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a> function to open the clipboard. The <b>EnumClipboardFormats</b> function fails if the clipboard is not open.

The
				<b>EnumClipboardFormats</b> function enumerates formats in the order that they were placed on the clipboard. If you are copying information to the clipboard, add clipboard objects in order from the most descriptive clipboard format to the least descriptive clipboard format. If you are pasting information from the clipboard, retrieve the first clipboard format that you can handle. That will be the most descriptive clipboard format that you can handle.

The system provides automatic type conversions for certain clipboard formats. In the case of such a format, this function enumerates the specified format, then enumerates the formats to which it can be converted. For more information, see <a href="clipboard_formats.htm">Standard Clipboard Formats</a>  and <a href="clipboard_formats.htm">Synthesized Clipboard Formats</a>.


#### Examples

For an example, see <a href="using_the_clipboard.htm">Example of a Clipboard Viewer</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3f9390f0-0fcb-4654-add0-eeea8f79b3f5">CountClipboardFormats</a>



<a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/892add91-a937-4602-86d2-5e5550a81872">RegisterClipboardFormat</a>
 

 

