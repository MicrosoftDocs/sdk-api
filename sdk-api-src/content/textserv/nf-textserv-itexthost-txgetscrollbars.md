---
UID: NF:textserv.ITextHost.TxGetScrollBars
title: ITextHost::TxGetScrollBars (textserv.h)
description: Requests information about the scroll bars supported by the text host.
helpviewer_keywords: ["ES_AUTOHSCROLL","ES_AUTOVSCROLL","ES_DISABLENOSCROLL","ITextHost interface [Windows Controls]","TxGetScrollBars method","ITextHost.TxGetScrollBars","ITextHost::TxGetScrollBars","TxGetScrollBars","TxGetScrollBars method [Windows Controls]","TxGetScrollBars method [Windows Controls]","ITextHost interface","WS_HSCROLL","WS_VSCROLL","_win32_ITextHost_TxGetScrollBars","_win32_ITextHost_TxGetScrollBars_cpp","controls.ITextHost_TxGetScrollBars","controls._win32_ITextHost_TxGetScrollBars","textserv/ITextHost::TxGetScrollBars"]
old-location: controls\ITextHost_TxGetScrollBars.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetscrollbars.htm
ms.date: 12/05/2018
ms.keywords: ES_AUTOHSCROLL, ES_AUTOVSCROLL, ES_DISABLENOSCROLL, ITextHost interface [Windows Controls],TxGetScrollBars method, ITextHost.TxGetScrollBars, ITextHost::TxGetScrollBars, TxGetScrollBars, TxGetScrollBars method [Windows Controls], TxGetScrollBars method [Windows Controls],ITextHost interface, WS_HSCROLL, WS_VSCROLL, _win32_ITextHost_TxGetScrollBars, _win32_ITextHost_TxGetScrollBars_cpp, controls.ITextHost_TxGetScrollBars, controls._win32_ITextHost_TxGetScrollBars, textserv/ITextHost::TxGetScrollBars
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
 - ITextHost::TxGetScrollBars
 - textserv/ITextHost::TxGetScrollBars
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
 - ITextHost.TxGetScrollBars
---

# ITextHost::TxGetScrollBars


## -description

Requests information about the scroll bars supported by the text host.

## -parameters

### -param pdwScrollBar

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The scroll bar. This parameter can be a combination of the following window styles related to scroll bars. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WS_VSCROLL"></a><a id="ws_vscroll"></a><dl>
<dt><b>WS_VSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Supports a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WS_HSCROLL"></a><a id="ws_hscroll"></a><dl>
<dt><b>WS_HSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Supports a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_AUTOVSCROLL"></a><a id="es_autovscroll"></a><dl>
<dt><b>ES_AUTOVSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Automatically scrolls text up one page when the user presses ENTER on the last line.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_AUTOHSCROLL"></a><a id="es_autohscroll"></a><dl>
<dt><b>ES_AUTOHSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Automatically scrolls text to the right by 10 characters when the user types a character at the end of the line. When the user presses ENTER, the control scrolls all text back to position zero.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_DISABLENOSCROLL"></a><a id="es_disablenoscroll"></a><dl>
<dt><b>ES_DISABLENOSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Disables scroll bars instead of hiding them when they are not needed.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>