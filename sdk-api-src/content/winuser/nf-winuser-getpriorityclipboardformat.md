---
UID: NF:winuser.GetPriorityClipboardFormat
title: GetPriorityClipboardFormat function (winuser.h)
description: Retrieves the first available clipboard format in the specified list.
helpviewer_keywords: ["GetPriorityClipboardFormat","GetPriorityClipboardFormat function [Data Exchange]","_win32_GetPriorityClipboardFormat","_win32_getpriorityclipboardformat_cpp","dataxchg.getpriorityclipboardformat","winui._win32_getpriorityclipboardformat","winuser/GetPriorityClipboardFormat"]
old-location: dataxchg\getpriorityclipboardformat.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getpriorityclipboardformat.htm
ms.date: 12/05/2018
ms.keywords: GetPriorityClipboardFormat, GetPriorityClipboardFormat function [Data Exchange], _win32_GetPriorityClipboardFormat, _win32_getpriorityclipboardformat_cpp, dataxchg.getpriorityclipboardformat, winui._win32_getpriorityclipboardformat, winuser/GetPriorityClipboardFormat
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
 - GetPriorityClipboardFormat
 - winuser/GetPriorityClipboardFormat
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
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetPriorityClipboardFormat
req.apiset: ext-ms-win-ntuser-misc-l1-5-1 (introduced in Windows 10, version 10.0.14393)
---

# GetPriorityClipboardFormat function


## -description

Retrieves the first available clipboard format in the specified list.

## -parameters

### -param paFormatPriorityList [in]

Type: <b>UINT*</b>

The clipboard formats, in priority order. For a description of the standard clipboard formats, see <a href="/windows/desktop/dataxchg/standard-clipboard-formats">Standard Clipboard Formats</a> .

### -param cFormats [in]

Type: <b>int</b>

The number of entries in the 
     <i>paFormatPriorityList</i> array. This value must not be greater than the number of entries in the list.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the first clipboard format in the list for which data is available. If the clipboard is empty, the return value is NULL. If the clipboard contains data, but not in any of the specified formats, the return value is –1. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-countclipboardformats">CountClipboardFormats</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumclipboardformats">EnumClipboardFormats</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclipboardformatnamea">GetClipboardFormatName</a>



<a href="/windows/desktop/api/winuser/nf-winuser-isclipboardformatavailable">IsClipboardFormatAvailable</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclipboardformata">RegisterClipboardFormat</a>
