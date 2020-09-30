---
UID: NF:textserv.ITextHost.TxCreateCaret
title: ITextHost::TxCreateCaret (textserv.h)
description: Creates a new shape for windowless rich edit control's caret.
helpviewer_keywords: ["CARET_CUSTOM","CARET_ITALIC","CARET_NONE","CARET_NULL","CARET_ROTATE90","CARET_RTL","ITextHost interface [Windows Controls]","TxCreateCaret method","ITextHost.TxCreateCaret","ITextHost::TxCreateCaret","TxCreateCaret","TxCreateCaret method [Windows Controls]","TxCreateCaret method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxCreateCaret","_win32_ITextHost_TxCreateCaret_cpp","controls.ITextHost_TxCreateCaret","controls._win32_ITextHost_TxCreateCaret","textserv/ITextHost::TxCreateCaret"]
old-location: controls\ITextHost_TxCreateCaret.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txcreatecaret.htm
ms.date: 12/05/2018
ms.keywords: CARET_CUSTOM, CARET_ITALIC, CARET_NONE, CARET_NULL, CARET_ROTATE90, CARET_RTL, ITextHost interface [Windows Controls],TxCreateCaret method, ITextHost.TxCreateCaret, ITextHost::TxCreateCaret, TxCreateCaret, TxCreateCaret method [Windows Controls], TxCreateCaret method [Windows Controls],ITextHost interface, _win32_ITextHost_TxCreateCaret, _win32_ITextHost_TxCreateCaret_cpp, controls.ITextHost_TxCreateCaret, controls._win32_ITextHost_TxCreateCaret, textserv/ITextHost::TxCreateCaret
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextHost::TxCreateCaret
 - textserv/ITextHost::TxCreateCaret
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost.TxCreateCaret
---

# ITextHost::TxCreateCaret


## -description

Creates a new shape for windowless rich edit control's caret.

## -parameters

### -param hbmp [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

Handle to the bitmap for the new caret shape. 


If the windowless rich edit control has the <a href="/windows/desktop/Controls/em-seteditstyle">SES_LOGICALCARET</a> style, <i>hbmp</i> is a combination of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CARET_CUSTOM"></a><a id="caret_custom"></a><dl>
<dt><b>CARET_CUSTOM</b></dt>
</dl>
</td>
<td width="60%">
An adorned caret. This value is valid only if CARET_RTL is also specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CARET_ITALIC"></a><a id="caret_italic"></a><dl>
<dt><b>CARET_ITALIC</b></dt>
</dl>
</td>
<td width="60%">
An italicized caret.

</td>
</tr>
<tr>
<td width="40%"><a id="CARET_NONE"></a><a id="caret_none"></a><dl>
<dt><b>CARET_NONE</b></dt>
</dl>
</td>
<td width="60%">
A blinking vertical bar.

</td>
</tr>
<tr>
<td width="40%"><a id="CARET_NULL"></a><a id="caret_null"></a><dl>
<dt><b>CARET_NULL</b></dt>
</dl>
</td>
<td width="60%">
An empty bitmap (for non-degenerate text selection).

</td>
</tr>
<tr>
<td width="40%"><a id="CARET_ROTATE90"></a><a id="caret_rotate90"></a><dl>
<dt><b>CARET_ROTATE90</b></dt>
</dl>
</td>
<td width="60%">
A caret that is rotated clockwise by 90 degrees.

</td>
</tr>
<tr>
<td width="40%"><a id="CARET_RTL"></a><a id="caret_rtl"></a><dl>
<dt><b>CARET_RTL</b></dt>
</dl>
</td>
<td width="60%">
The caret moves right to left.

</td>
</tr>
</table>

### -param xWidth [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Caret width, in logical units.

### -param yHeight [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Caret height, in logical units.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails.

## -remarks

This method is only valid when the control is in-place active; calls while the control is inactive may fail.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createcaret">CreateCaret</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Other Resources</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>