---
UID: NF:winuser.SetSystemCursor
title: SetSystemCursor function (winuser.h)
description: Enables an application to customize the system cursors. It replaces the contents of the system cursor specified by the id parameter with the contents of the cursor specified by the hcur parameter and then destroys hcur.
helpviewer_keywords: ["OCR_APPSTARTING","OCR_CROSS","OCR_HAND","OCR_HELP","OCR_IBEAM","OCR_NO","OCR_NORMAL","OCR_SIZEALL","OCR_SIZENESW","OCR_SIZENS","OCR_SIZENWSE","OCR_SIZEWE","OCR_UP","OCR_WAIT","SetSystemCursor","SetSystemCursor function [Menus and Other Resources]","_win32_SetSystemCursor","_win32_setsystemcursor_cpp","menurc.setsystemcursor","winui._win32_setsystemcursor","winuser/SetSystemCursor"]
old-location: menurc\setsystemcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\setsystemcursor.htm
ms.date: 12/05/2018
ms.keywords: OCR_APPSTARTING, OCR_CROSS, OCR_HAND, OCR_HELP, OCR_IBEAM, OCR_NO, OCR_NORMAL, OCR_SIZEALL, OCR_SIZENESW, OCR_SIZENS, OCR_SIZENWSE, OCR_SIZEWE, OCR_UP, OCR_WAIT, SetSystemCursor, SetSystemCursor function [Menus and Other Resources], _win32_SetSystemCursor, _win32_setsystemcursor_cpp, menurc.setsystemcursor, winui._win32_setsystemcursor, winuser/SetSystemCursor
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
 - SetSystemCursor
 - winuser/SetSystemCursor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetSystemCursor
---

# SetSystemCursor function


## -description

Enables an application to customize the system cursors. It replaces the contents of the system cursor specified by the <i>id</i> parameter with the contents of the cursor specified by the <i>hcur</i> parameter and then destroys <i>hcur</i>.

## -parameters

### -param hcur [in]

Type: <b>HCURSOR</b>

A handle to the cursor. The function replaces the contents of the system cursor specified by <i>id</i> with the contents of the cursor handled by <i>hcur</i>.

The system destroys <i>hcur</i> by calling the <a href="/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a> function. Therefore, <i>hcur</i> cannot be a cursor loaded using the <a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a> function. To specify a cursor loaded from a resource, copy the cursor using the <a href="/windows/desktop/api/winuser/nf-winuser-copycursor">CopyCursor</a> function, then pass the copy to <b>SetSystemCursor</b>.

### -param id [in]

Type: <b>DWORD</b>

The system cursor to replace with the contents of <i>hcur</i>. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OCR_APPSTARTING"></a><a id="ocr_appstarting"></a><dl>
<dt><b>OCR_APPSTARTING</b></dt>
<dt>32650</dt>
</dl>
</td>
<td width="60%">
Standard arrow and small hourglass

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_NORMAL"></a><a id="ocr_normal"></a><dl>
<dt><b>OCR_NORMAL</b></dt>
<dt>32512</dt>
</dl>
</td>
<td width="60%">
Standard arrow

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_CROSS"></a><a id="ocr_cross"></a><dl>
<dt><b>OCR_CROSS</b></dt>
<dt>32515</dt>
</dl>
</td>
<td width="60%">
Crosshair

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_HAND"></a><a id="ocr_hand"></a><dl>
<dt><b>OCR_HAND</b></dt>
<dt>32649</dt>
</dl>
</td>
<td width="60%">
Hand

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_HELP"></a><a id="ocr_help"></a><dl>
<dt><b>OCR_HELP</b></dt>
<dt>32651</dt>
</dl>
</td>
<td width="60%">
Arrow and question mark

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_IBEAM"></a><a id="ocr_ibeam"></a><dl>
<dt><b>OCR_IBEAM</b></dt>
<dt>32513</dt>
</dl>
</td>
<td width="60%">
I-beam

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_NO"></a><a id="ocr_no"></a><dl>
<dt><b>OCR_NO</b></dt>
<dt>32648</dt>
</dl>
</td>
<td width="60%">
Slashed circle

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_SIZEALL"></a><a id="ocr_sizeall"></a><dl>
<dt><b>OCR_SIZEALL</b></dt>
<dt>32646</dt>
</dl>
</td>
<td width="60%">
Four-pointed arrow pointing north, south, east, and west

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_SIZENESW"></a><a id="ocr_sizenesw"></a><dl>
<dt><b>OCR_SIZENESW</b></dt>
<dt>32643</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow pointing northeast and southwest

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_SIZENS"></a><a id="ocr_sizens"></a><dl>
<dt><b>OCR_SIZENS</b></dt>
<dt>32645</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow pointing north and south

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_SIZENWSE"></a><a id="ocr_sizenwse"></a><dl>
<dt><b>OCR_SIZENWSE</b></dt>
<dt>32642</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow pointing northwest and southeast

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_SIZEWE"></a><a id="ocr_sizewe"></a><dl>
<dt><b>OCR_SIZEWE</b></dt>
<dt>32644</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow pointing west and east

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_UP"></a><a id="ocr_up"></a><dl>
<dt><b>OCR_UP</b></dt>
<dt>32516</dt>
</dl>
</td>
<td width="60%">
Vertical arrow

</td>
</tr>
<tr>
<td width="40%"><a id="OCR_WAIT"></a><a id="ocr_wait"></a><dl>
<dt><b>OCR_WAIT</b></dt>
<dt>32514</dt>
</dl>
</td>
<td width="60%">
Hourglass

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For an application to use any of the OCR_ constants, the constant <b>OEMRESOURCE</b> must be defined before the Windows.h header file is included.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursorfromfilea">LoadCursorFromFile</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>