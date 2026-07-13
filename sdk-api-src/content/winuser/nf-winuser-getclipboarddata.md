---
UID: NF:winuser.GetClipboardData
title: GetClipboardData function (winuser.h)
description: Retrieves data from the clipboard in a specified format. The clipboard must have been opened previously.
helpviewer_keywords: ["GetClipboardData","GetClipboardData function [Data Exchange]","_win32_GetClipboardData","_win32_getclipboarddata_cpp","dataxchg.getclipboarddata","winui._win32_getclipboarddata","winuser/GetClipboardData"]
old-location: dataxchg\getclipboarddata.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getclipboarddata.htm
ms.date: 12/05/2018
ms.keywords: GetClipboardData, GetClipboardData function [Data Exchange], _win32_GetClipboardData, _win32_getclipboarddata_cpp, dataxchg.getclipboarddata, winui._win32_getclipboarddata, winuser/GetClipboardData
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
 - GetClipboardData
 - winuser/GetClipboardData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-misc-l1-1-0.dll
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetClipboardData
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# GetClipboardData function


## -description

Retrieves data from the clipboard in a specified format. The clipboard must have been opened previously.

## -parameters

### -param uFormat [in]

Type: <b>UINT</b>

A clipboard format. For a description of the standard clipboard formats, see <a href="/windows/desktop/dataxchg/clipboard-formats">Standard Clipboard Formats</a>.

## -returns

Type: <b>HANDLE</b>

If the function succeeds, the return value is the handle to a clipboard object in the specified format.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Caution</b>  Clipboard data is not trusted. Parse the data carefully before using it in your application.</div>
<div> </div>
An application can enumerate the available formats in advance by using the <a href="/windows/desktop/api/winuser/nf-winuser-enumclipboardformats">EnumClipboardFormats</a> function. 

The clipboard controls the handle that the <b>GetClipboardData</b> function returns, not the application. The application should copy the data immediately. The application must not free the handle nor leave it locked. The application must not use the handle after the <a href="/windows/desktop/api/winuser/nf-winuser-emptyclipboard">EmptyClipboard</a> or <a href="/windows/desktop/api/winuser/nf-winuser-closeclipboard">CloseClipboard</a> function is called, or after the <a href="/windows/desktop/api/winuser/nf-winuser-setclipboarddata">SetClipboardData</a> function is called with the same clipboard format. 

The system performs implicit data format conversions between certain clipboard formats when an application calls the <b>GetClipboardData</b> function. For example, if the <a href="/windows/desktop/dataxchg/standard-clipboard-formats">CF_OEMTEXT</a> format is on the clipboard, a window can retrieve data in the <a href="/windows/desktop/dataxchg/standard-clipboard-formats">CF_TEXT</a> format. The format on the clipboard is converted to the requested format on demand. For more information, see <a href="/windows/desktop/dataxchg/clipboard-formats">Synthesized Clipboard Formats</a>. 


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Copying Information to the Clipboard</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<a href="/windows/desktop/api/winuser/nf-winuser-closeclipboard">CloseClipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-emptyclipboard">EmptyClipboard</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumclipboardformats">EnumClipboardFormats</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setclipboarddata">SetClipboardData</a>
