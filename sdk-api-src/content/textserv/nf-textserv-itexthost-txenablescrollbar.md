---
UID: NF:textserv.ITextHost.TxEnableScrollBar
title: ITextHost::TxEnableScrollBar (textserv.h)
description: Enables or disables one or both scroll bar arrows in the text host window.
helpviewer_keywords: ["ESB_DISABLE_BOTH","ESB_DISABLE_DOWN","ESB_DISABLE_LEFT","ESB_DISABLE_LTUP","ESB_DISABLE_RIGHT","ESB_DISABLE_RTDN","ESB_DISABLE_UP","ESB_ENABLE_BOTH","ITextHost interface [Windows Controls]","TxEnableScrollBar method","ITextHost.TxEnableScrollBar","ITextHost::TxEnableScrollBar","SB_BOTH","SB_HORZ","SB_VERT","TxEnableScrollBar","TxEnableScrollBar method [Windows Controls]","TxEnableScrollBar method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxEnableScrollBar","_win32_ITextHost_TxEnableScrollBar_cpp","controls.ITextHost_TxEnableScrollBar","controls._win32_ITextHost_TxEnableScrollBar","textserv/ITextHost::TxEnableScrollBar"]
old-location: controls\ITextHost_TxEnableScrollBar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txenablescrollbar.htm
ms.date: 12/05/2018
ms.keywords: ESB_DISABLE_BOTH, ESB_DISABLE_DOWN, ESB_DISABLE_LEFT, ESB_DISABLE_LTUP, ESB_DISABLE_RIGHT, ESB_DISABLE_RTDN, ESB_DISABLE_UP, ESB_ENABLE_BOTH, ITextHost interface [Windows Controls],TxEnableScrollBar method, ITextHost.TxEnableScrollBar, ITextHost::TxEnableScrollBar, SB_BOTH, SB_HORZ, SB_VERT, TxEnableScrollBar, TxEnableScrollBar method [Windows Controls], TxEnableScrollBar method [Windows Controls],ITextHost interface, _win32_ITextHost_TxEnableScrollBar, _win32_ITextHost_TxEnableScrollBar_cpp, controls.ITextHost_TxEnableScrollBar, controls._win32_ITextHost_TxEnableScrollBar, textserv/ITextHost::TxEnableScrollBar
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
 - ITextHost::TxEnableScrollBar
 - textserv/ITextHost::TxEnableScrollBar
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
 - ITextHost.TxEnableScrollBar
---

# ITextHost::TxEnableScrollBar


## -description

Enables or disables one or both scroll bar arrows in the text host window.

## -parameters

### -param fuSBFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Specifies which scroll bar is affected. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SB_BOTH"></a><a id="sb_both"></a><dl>
<dt><b>SB_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Affects both the horizontal and vertical scroll bars.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Affects the horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Affects the vertical scroll bar.

</td>
</tr>
</table>

### -param fuArrowflags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Specifies which scroll bar arrows are enabled or disabled. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_BOTH"></a><a id="esb_disable_both"></a><dl>
<dt><b>ESB_DISABLE_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Disables both arrows on a scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_DOWN"></a><a id="esb_disable_down"></a><dl>
<dt><b>ESB_DISABLE_DOWN</b></dt>
</dl>
</td>
<td width="60%">
Disables the down arrow on a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_LEFT"></a><a id="esb_disable_left"></a><dl>
<dt><b>ESB_DISABLE_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Disables the left arrow on a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_LTUP"></a><a id="esb_disable_ltup"></a><dl>
<dt><b>ESB_DISABLE_LTUP</b></dt>
</dl>
</td>
<td width="60%">
Disables the left arrow on a horizontal scroll bar or the up arrow of a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_RIGHT"></a><a id="esb_disable_right"></a><dl>
<dt><b>ESB_DISABLE_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Disables the right arrow on a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_RTDN"></a><a id="esb_disable_rtdn"></a><dl>
<dt><b>ESB_DISABLE_RTDN</b></dt>
</dl>
</td>
<td width="60%">
Disables the right arrow on a horizontal scroll bar or the down arrow of a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_UP"></a><a id="esb_disable_up"></a><dl>
<dt><b>ESB_DISABLE_UP</b></dt>
</dl>
</td>
<td width="60%">
Disables the up arrow on a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_ENABLE_BOTH"></a><a id="esb_enable_both"></a><dl>
<dt><b>ESB_ENABLE_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Enables both arrows on a scroll bar.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Return nonzero if the arrows are enabled or disabled as specified. 

Return zero if the arrows are already in the requested state or an error occurs.

## -remarks

This method is only valid when the control is in-place active; calls while the control is inactive may fail.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>