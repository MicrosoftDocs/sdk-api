---
UID: NF:winuser.IsClipboardFormatAvailable
title: IsClipboardFormatAvailable function (winuser.h)
description: Determines whether the clipboard contains data in the specified format.
helpviewer_keywords: ["IsClipboardFormatAvailable","IsClipboardFormatAvailable function [Data Exchange]","_win32_IsClipboardFormatAvailable","_win32_isclipboardformatavailable_cpp","dataxchg.isclipboardformatavailable","winui._win32_isclipboardformatavailable","winuser/IsClipboardFormatAvailable"]
old-location: dataxchg\isclipboardformatavailable.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\isclipboardformatavailable.htm
ms.date: 12/05/2018
ms.keywords: IsClipboardFormatAvailable, IsClipboardFormatAvailable function [Data Exchange], _win32_IsClipboardFormatAvailable, _win32_isclipboardformatavailable_cpp, dataxchg.isclipboardformatavailable, winui._win32_isclipboardformatavailable, winuser/IsClipboardFormatAvailable
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
 - IsClipboardFormatAvailable
 - winuser/IsClipboardFormatAvailable
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
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# IsClipboardFormatAvailable function


## -description

Determines whether the clipboard contains data in the specified format.

## -parameters

### -param format [in]

Type: <b>UINT</b>

A standard or registered clipboard format. For a description of the standard clipboard formats, see <a href="/windows/desktop/dataxchg/standard-clipboard-formats">Standard Clipboard Formats</a> .

## -returns

Type: <b>BOOL</b>

If the clipboard format is available, the return value is nonzero.

If the clipboard format is not available, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Typically, an application that recognizes only one clipboard format would call this function when processing the <a href="/windows/desktop/menurc/wm-initmenu">WM_INITMENU</a> or <a href="/windows/desktop/menurc/wm-initmenupopup">WM_INITMENUPOPUP</a> message. The application would then enable or disable the Paste menu item, depending on the return value. Applications that recognize more than one clipboard format should use the <a href="/windows/desktop/api/winuser/nf-winuser-getpriorityclipboardformat">GetPriorityClipboardFormat</a> function for this purpose. 


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Pasting Information from the Clipboard</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-countclipboardformats">CountClipboardFormats</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumclipboardformats">EnumClipboardFormats</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getpriorityclipboardformat">GetPriorityClipboardFormat</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclipboardformata">RegisterClipboardFormat</a>



<a href="/windows/desktop/menurc/wm-initmenu">WM_INITMENU</a>



<a href="/windows/desktop/menurc/wm-initmenupopup">WM_INITMENUPOPUP</a>
