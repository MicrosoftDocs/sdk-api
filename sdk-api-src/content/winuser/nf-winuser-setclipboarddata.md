---
UID: NF:winuser.SetClipboardData
title: SetClipboardData function (winuser.h)
description: Places data on the clipboard in a specified clipboard format.
helpviewer_keywords: ["SetClipboardData","SetClipboardData function [Data Exchange]","_win32_SetClipboardData","_win32_setclipboarddata_cpp","dataxchg.setclipboarddata","winui._win32_setclipboarddata","winuser/SetClipboardData"]
old-location: dataxchg\setclipboarddata.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\setclipboarddata.htm
ms.date: 12/05/2018
ms.keywords: SetClipboardData, SetClipboardData function [Data Exchange], _win32_SetClipboardData, _win32_setclipboarddata_cpp, dataxchg.setclipboarddata, winui._win32_setclipboarddata, winuser/SetClipboardData
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
 - SetClipboardData
 - winuser/SetClipboardData
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
 - SetClipboardData
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# SetClipboardData function


## -description

Places data on the clipboard in a specified clipboard format. The window must be the current clipboard owner, and the application must have called the [**OpenClipboard**](nf-winuser-openclipboard.md) function. (When responding to the [WM_RENDERFORMAT](/windows/win32/dataxchg/wm-renderformat) message, the clipboard owner must not call **OpenClipboard** before calling **SetClipboardData**.)

## -parameters

### -param uFormat [in]

Type: <b>UINT</b>

The clipboard format. This parameter can be a registered format or any of the standard clipboard formats. For more information, see <a href="/windows/desktop/dataxchg/standard-clipboard-formats">Standard Clipboard Formats</a> and <a href="/windows/desktop/dataxchg/clipboard-formats">Registered Clipboard Formats</a>.

### -param hMem [in, optional]

Type: <b>HANDLE</b>

A handle to the data in the specified format. This parameter can be <b>NULL</b>, indicating that the window provides data in the specified clipboard format (renders the format) upon request; this is known as [delayed rendering](/windows/win32/dataxchg/clipboard-operations#delayed-rendering). If a window delays rendering, it must process the [WM_RENDERFORMAT](/windows/win32/dataxchg/wm-renderformat) and [WM_RENDERALLFORMATS](/windows/win32/dataxchg/wm-renderallformats) messages.

If <b>SetClipboardData</b> succeeds, the system owns the object identified by the <i>hMem</i> parameter. The application may not write to or free the data once ownership has been transferred to the system, but it can lock and read from the data until the <a href="/windows/desktop/api/winuser/nf-winuser-closeclipboard">CloseClipboard</a> function is called. (The memory must be unlocked before the Clipboard is closed.) If the <i>hMem</i> parameter identifies a memory object, the object must have been allocated using the function with the <b>GMEM_MOVEABLE</b> flag.

## -returns

Type: <b>HANDLE</b>

If the function succeeds, the return value is the handle to the data.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>Windows 8:</b> Bitmaps to be shared with Windows Store app apps must be in the <b>CF_BITMAP</b> format (device-dependent bitmap). 

If an application calls <b>SetClipboardData</b> in response to <a href="/windows/desktop/dataxchg/wm-renderformat">WM_RENDERFORMAT</a> or <a href="/windows/desktop/dataxchg/wm-renderallformats">WM_RENDERALLFORMATS</a>, the application should not use the handle after <b>SetClipboardData</b> has been called.

If an application calls <a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a> with hwnd set to <b>NULL</b>, <a href="/windows/desktop/api/winuser/nf-winuser-emptyclipboard">EmptyClipboard</a> sets the clipboard owner to <b>NULL</b>; this causes <b>SetClipboardData</b> to fail.

The system performs implicit data format conversions between certain clipboard formats when an application calls the <a href="/windows/desktop/api/winuser/nf-winuser-getclipboarddata">GetClipboardData</a> function. For example, if the <b>CF_OEMTEXT</b> format is on the clipboard, a window can retrieve data in the <b>CF_TEXT</b> format. The format on the clipboard is converted to the requested format on demand. For more information, see <a href="/windows/desktop/dataxchg/clipboard-formats">Synthesized Clipboard Formats</a>.


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Copying Information to the Clipboard</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<a href="/windows/desktop/api/winuser/nf-winuser-closeclipboard">CloseClipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclipboarddata">GetClipboardData</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclipboardformata">RegisterClipboardFormat</a>



<a href="/windows/desktop/dataxchg/wm-renderallformats">WM_RENDERALLFORMATS</a>



<a href="/windows/desktop/dataxchg/wm-renderformat">WM_RENDERFORMAT</a>
