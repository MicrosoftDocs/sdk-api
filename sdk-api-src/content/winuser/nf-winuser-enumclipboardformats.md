---
UID: NF:winuser.EnumClipboardFormats
title: EnumClipboardFormats function (winuser.h)
description: Enumerates the data formats currently available on the clipboard.
helpviewer_keywords: ["EnumClipboardFormats","EnumClipboardFormats function [Data Exchange]","_win32_EnumClipboardFormats","_win32_enumclipboardformats_cpp","dataxchg.enumclipboardformats","winui._win32_enumclipboardformats","winuser/EnumClipboardFormats"]
old-location: dataxchg\enumclipboardformats.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\enumclipboardformats.htm
ms.date: 12/05/2018
ms.keywords: EnumClipboardFormats, EnumClipboardFormats function [Data Exchange], _win32_EnumClipboardFormats, _win32_enumclipboardformats_cpp, dataxchg.enumclipboardformats, winui._win32_enumclipboardformats, winuser/EnumClipboardFormats
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumClipboardFormats
 - winuser/EnumClipboardFormats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
api_name:
 - EnumClipboardFormats
req.apiset: ext-ms-win-ntuser-misc-l1-5-1 (introduced in Windows 10, version 10.0.14393)
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

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the clipboard is not open, the function fails. 

If there are no more clipboard formats to enumerate, the return value is zero. In this case, the 
						<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the value <b>ERROR_SUCCESS</b>. This lets you distinguish between function failure and the end of enumeration.

## -remarks

You must open the clipboard before enumerating its formats. Use the <a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a> function to open the clipboard. The <b>EnumClipboardFormats</b> function fails if the clipboard is not open.

The
				<b>EnumClipboardFormats</b> function enumerates formats in the order that they were placed on the clipboard. If you are copying information to the clipboard, add clipboard objects in order from the most descriptive clipboard format to the least descriptive clipboard format. If you are pasting information from the clipboard, retrieve the first clipboard format that you can handle. That will be the most descriptive clipboard format that you can handle.

The system provides automatic type conversions for certain clipboard formats. In the case of such a format, this function enumerates the specified format, then enumerates the formats to which it can be converted. For more information, see <a href="/windows/desktop/dataxchg/clipboard-formats">Standard Clipboard Formats</a>  and <a href="/windows/desktop/dataxchg/clipboard-formats">Synthesized Clipboard Formats</a>.


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Example of a Clipboard Viewer</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-countclipboardformats">CountClipboardFormats</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclipboardformata">RegisterClipboardFormat</a>
