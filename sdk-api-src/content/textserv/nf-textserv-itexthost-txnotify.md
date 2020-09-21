---
UID: NF:textserv.ITextHost.TxNotify
title: ITextHost::TxNotify (textserv.h)
description: Notifies the text host of various events.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxNotify method","ITextHost.TxNotify","ITextHost::TxNotify","TxNotify","TxNotify method [Windows Controls]","TxNotify method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxNotify","_win32_ITextHost_TxNotify_cpp","controls.ITextHost_TxNotify","controls._win32_ITextHost_TxNotify","textserv/ITextHost::TxNotify"]
old-location: controls\ITextHost_TxNotify.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxnotify.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxNotify method, ITextHost.TxNotify, ITextHost::TxNotify, TxNotify, TxNotify method [Windows Controls], TxNotify method [Windows Controls],ITextHost interface, _win32_ITextHost_TxNotify, _win32_ITextHost_TxNotify_cpp, controls.ITextHost_TxNotify, controls._win32_ITextHost_TxNotify, textserv/ITextHost::TxNotify
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
 - ITextHost::TxNotify
 - textserv/ITextHost::TxNotify
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
 - ITextHost.TxNotify
---

# ITextHost::TxNotify


## -description

Notifies the text host of various events.

## -parameters

### -param iNotify [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Event to notify host of. One of the 
					<b>EN_</b> notification codes.

### -param pv [in]

Type: <b>void*</b>

Extra data, dependent on 
					<i>iNotify</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Return S_OK if the method succeeds. 

Return S_FALSE if the method fails. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

Note that there are two basic categories of events, 
				<i>direct</i> and 
				<i>delayed</i> . Direct events are sent immediately because they need some processing, for example, <a href="/windows/desktop/Controls/en-protected">EN_PROTECTED</a>. Delayed events are sent after all processing has occurred; the control is thus in a stable state. Examples of delayed notifications are <a href="/windows/desktop/Controls/en-change">EN_CHANGE</a>, <a href="/windows/desktop/Controls/en-errspace">EN_ERRSPACE</a>, and <a href="/windows/desktop/Controls/en-selchange">EN_SELCHANGE</a>.

The notification events are the same as the notification codes sent to the parent window of a rich edit window. The firing of events may be controlled with a mask set through the <a href="/windows/desktop/Controls/em-seteventmask">EM_SETEVENTMASK</a> message.

In general, it is legal to make calls to the text services object while processing this method; however, implementers are cautioned to avoid excessive recursion.

The following is a list of the notifications that may be sent.

<table class="clsStd">
<tr>
<th>Notification</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-change">EN_CHANGE</a>
</td>
<td>Sent after the system updates the screen, when the user takes an action that may have altered text in the control. </td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-dropfiles">EN_DROPFILES</a>
</td>
<td>Sent when either a 
							<a href="/windows/desktop/shell/wm-dropfiles">WM_DROPFILES</a> message or an 
							<a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> notification is received.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-errspace">EN_ERRSPACE</a>
</td>
<td>Sent when a control cannot allocate enough memory to meet a specified request.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-hscroll">EN_HSCROLL</a>
</td>
<td>Sent when the user clicks the control's horizontal scroll bar before the screen is updated.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-killfocus">EN_KILLFOCUS</a>
</td>
<td>Sent when the control loses the keyboard focus.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-link">EN_LINK</a>
</td>
<td>Sent when a rich edit control receives various messages, such as mouse click messages, when the mouse pointer is over text that has the CFE_LINK effect. </td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-maxtext">EN_MAXTEXT</a>
</td>
<td>Sent when the current text insertion has exceeded the maximum number of characters for the control.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-oleopfailed">EN_OLEOPFAILED</a>
</td>
<td>Sent when a user action on an OLE object has failed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-protected">EN_PROTECTED</a>
</td>
<td>Sent when the user takes an action that changes the protected range of text.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-requestresize">EN_REQUESTRESIZE</a>
</td>
<td>Sent when a rich edit control's contents are different from the control's window size. </td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-saveclipboard">EN_SAVECLIPBOARD</a>
</td>
<td>Sent when an edit control is being destroyed. The text host should indicate whether <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> should be called. Data indicating the number of characters and objects to be flushed is sent in the 
							<a href="/windows/desktop/api/richedit/ns-richedit-ensaveclipboard">ENSAVECLIPBOARD</a> data structure. Mask value is nothing.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-selchange">EN_SELCHANGE</a>
</td>
<td>Sent when the current selection has changed. A <a href="/windows/desktop/api/richedit/ns-richedit-selchange">SELCHANGE</a> data structure is also sent, which indicates the new selection range at the type of data the selection is currently over. Controlled through the <a href="/windows/desktop/Controls/rich-edit-control-event-mask-flags">ENM_SELCHANGE</a> mask.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-setfocus">EN_SETFOCUS</a>
</td>
<td>Sent when the edit control receives the keyboard focus. No extra data is sent; there is no mask.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-stopnoundo">EN_STOPNOUNDO</a>
</td>
<td>Sent when an action occurs for which the control cannot allocate enough memory to maintain the undo state. If S_FALSE is returned, the action will be stopped; otherwise, the action will continue.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-update">EN_UPDATE</a>
</td>
<td>Sent before an edit control requests a redraw of altered data or text. No additional data is sent. This event is controlled through the <a href="/windows/desktop/Controls/rich-edit-control-event-mask-flags">ENM_UPDATE</a> mask. 
							<b>Rich Edit 2.0 and later:</b> The <a href="/windows/desktop/Controls/rich-edit-control-event-mask-flags">ENM_UPDATE</a> mask is ignored and the <a href="/windows/desktop/Controls/en-update">EN_UPDATE</a> notification code is always sent. However, when Microsoft Rich Edit 3.0 emulates Microsoft Rich Edit 1.0, the <b>ENM_UPDATE</b> mask controls this notification.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/Controls/en-vscroll">EN_VSCROLL</a>
</td>
<td>Sent when the user clicks an edit control's vertical scroll bar or when the user scrolls the mouse wheel over the edit control, before the screen is updated. This is controlled through the <a href="/windows/desktop/Controls/rich-edit-control-event-mask-flags">ENM_SCROLL</a> mask; no extra data is sent.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/Controls/en-msgfilter">EN_MSGFILTER</a> is not sent to <b>TxNotify</b>. To filter window messages, use <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-txsendmessage">TxSendMessage</a>.</div>
<div> </div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/Controls/em-seteventmask">EM_SETEVENTMASK</a>



<a href="/windows/desktop/Controls/en-change">EN_CHANGE</a>



<a href="/windows/desktop/Controls/en-dropfiles">EN_DROPFILES</a>



<a href="/windows/desktop/Controls/en-errspace">EN_ERRSPACE</a>



<a href="/windows/desktop/Controls/en-hscroll">EN_HSCROLL</a>



<a href="/windows/desktop/Controls/en-killfocus">EN_KILLFOCUS</a>



<a href="/windows/desktop/Controls/en-link">EN_LINK</a>



<a href="/windows/desktop/Controls/en-maxtext">EN_MAXTEXT</a>



<a href="/windows/desktop/Controls/en-oleopfailed">EN_OLEOPFAILED</a>



<a href="/windows/desktop/Controls/en-protected">EN_PROTECTED</a>



<a href="/windows/desktop/Controls/en-requestresize">EN_REQUESTRESIZE</a>



<a href="/windows/desktop/Controls/en-saveclipboard">EN_SAVECLIPBOARD</a>



<a href="/windows/desktop/Controls/en-selchange">EN_SELCHANGE</a>



<a href="/windows/desktop/Controls/en-setfocus">EN_SETFOCUS</a>



<a href="/windows/desktop/Controls/en-stopnoundo">EN_STOPNOUNDO</a>



<a href="/windows/desktop/Controls/en-update">EN_UPDATE</a>



<a href="/windows/desktop/Controls/en-vscroll">EN_VSCROLL</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>