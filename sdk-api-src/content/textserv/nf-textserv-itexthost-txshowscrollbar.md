---
UID: NF:textserv.ITextHost.TxShowScrollBar
title: ITextHost::TxShowScrollBar (textserv.h)
description: Shows or hides the scroll bar in the text host window.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxShowScrollBar method","ITextHost.TxShowScrollBar","ITextHost::TxShowScrollBar","TxShowScrollBar","TxShowScrollBar method [Windows Controls]","TxShowScrollBar method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxShowScrollBar","_win32_ITextHost_TxShowScrollBar_cpp","controls.ITextHost_TxShowScrollBar","controls._win32_ITextHost_TxShowScrollBar","textserv/ITextHost::TxShowScrollBar"]
old-location: controls\ITextHost_TxShowScrollBar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txshowscrollbar.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxShowScrollBar method, ITextHost.TxShowScrollBar, ITextHost::TxShowScrollBar, TxShowScrollBar, TxShowScrollBar method [Windows Controls], TxShowScrollBar method [Windows Controls],ITextHost interface, _win32_ITextHost_TxShowScrollBar, _win32_ITextHost_TxShowScrollBar_cpp, controls.ITextHost_TxShowScrollBar, controls._win32_ITextHost_TxShowScrollBar, textserv/ITextHost::TxShowScrollBar
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
 - ITextHost::TxShowScrollBar
 - textserv/ITextHost::TxShowScrollBar
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
 - ITextHost.TxShowScrollBar
---

# ITextHost::TxShowScrollBar


## -description

Shows or hides the scroll bar in the text host window.

## -parameters

### -param fnBar [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Specifies the scroll bar(s) to be shown or hidden. This parameter can be one of the following values. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SB_BOTH</td>
<td>Shows or hides a window's standard horizontal and vertical scroll bars.</td>
</tr>
<tr>
<td>SB_HORZ</td>
<td>Shows or hides a window's standard horizontal scroll bars.</td>
</tr>
<tr>
<td>SB_VERT</td>
<td>Shows or hides a window's standard vertical scroll bar.</td>
</tr>
</table>

### -param fShow [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Flag. If <b>TRUE</b>, the scroll bars indicated by <i>fnBar</i> is visible. If <b>FALSE</b>, the scroll bar is hidden.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails.

## -remarks

This method is only valid when the control is in-place active; calls while the control is inactive may fail.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>