---
UID: NF:textserv.ITextHost.TxNotify
title: ITextHost::TxNotify
author: windows-sdk-content
description: Notifies the text host of various events.
old-location: controls\ITextHost_TxNotify.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxnotify.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITextHost interface [Windows Controls],TxNotify method, ITextHost.TxNotify, ITextHost::TxNotify, TxNotify, TxNotify method [Windows Controls], TxNotify method [Windows Controls],ITextHost interface, _win32_ITextHost_TxNotify, _win32_ITextHost_TxNotify_cpp, controls.ITextHost_TxNotify, controls._win32_ITextHost_TxNotify, textserv/ITextHost::TxNotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost.TxNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- textserv.h
: 
- ITextHost.TxNotify
: 
---

# ITextHost::TxNotify


## -description


Notifies the text host of various events. 


## -parameters




### -param iNotify [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Event to notify host of. One of the 
					<b>EN_</b> notification codes. 


### -param pv [in]

Type: <b>void*</b>

Extra data, dependent on 
					<i>iNotify</i>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Return S_OK if the method succeeds. 

Return S_FALSE if the method fails. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>. 




## -remarks



Note that there are two basic categories of events, 
				<i>direct</i> and 
				<i>delayed</i> . Direct events are sent immediately because they need some processing, for example, <a href="https://msdn.microsoft.com/en-us/library/Bb787981(v=VS.85).aspx">EN_PROTECTED</a>. Delayed events are sent after all processing has occurred; the control is thus in a stable state. Examples of delayed notifications are <a href="https://msdn.microsoft.com/en-us/library/Bb761676(v=VS.85).aspx">EN_CHANGE</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb761678(v=VS.85).aspx">EN_ERRSPACE</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb787987(v=VS.85).aspx">EN_SELCHANGE</a>.

The notification events are the same as the notification codes sent to the parent window of a rich edit window. The firing of events may be controlled with a mask set through the <a href="https://msdn.microsoft.com/en-us/library/Bb774238(v=VS.85).aspx">EM_SETEVENTMASK</a> message.

In general, it is legal to make calls to the text services object while processing this method; however, implementers are cautioned to avoid excessive recursion.

The following is a list of the notifications that may be sent.

<table class="clsStd">
<tr>
<th>Notification</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb761676(v=VS.85).aspx">EN_CHANGE</a>
</td>
<td>Sent after the system updates the screen, when the user takes an action that may have altered text in the control. </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb787966(v=VS.85).aspx">EN_DROPFILES</a>
</td>
<td>Sent when either a 
							<a href="https://msdn.microsoft.com/07dc2df7-4699-4e9c-b1a5-4ce877116268">WM_DROPFILES</a> message or an 
							<a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a> notification is received.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb761678(v=VS.85).aspx">EN_ERRSPACE</a>
</td>
<td>Sent when a control cannot allocate enough memory to meet a specified request.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb761680(v=VS.85).aspx">EN_HSCROLL</a>
</td>
<td>Sent when the user clicks the control's horizontal scroll bar before the screen is updated.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb761682(v=VS.85).aspx">EN_KILLFOCUS</a>
</td>
<td>Sent when the control loses the keyboard focus.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb787970(v=VS.85).aspx">EN_LINK</a>
</td>
<td>Sent when a rich edit control receives various messages, such as mouse click messages, when the mouse pointer is over text that has the CFE_LINK effect. </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb761684(v=VS.85).aspx">EN_MAXTEXT</a>
</td>
<td>Sent when the current text insertion has exceeded the maximum number of characters for the control.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb787979(v=VS.85).aspx">EN_OLEOPFAILED</a>
</td>
<td>Sent when a user action on an OLE object has failed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb787981(v=VS.85).aspx">EN_PROTECTED</a>
</td>
<td>Sent when the user takes an action that changes the protected range of text.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb787983(v=VS.85).aspx">EN_REQUESTRESIZE</a>
</td>
<td>Sent when a rich edit control's contents are different from the control's window size. </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb787985(v=VS.85).aspx">EN_SAVECLIPBOARD</a>
</td>
<td>Sent when an edit control is being destroyed. The text host should indicate whether <a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a> should be called. Data indicating the number of characters and objects to be flushed is sent in the 
							<a href="https://msdn.microsoft.com/en-us/library/Bb787905(v=VS.85).aspx">ENSAVECLIPBOARD</a> data structure. Mask value is nothing.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb787987(v=VS.85).aspx">EN_SELCHANGE</a>
</td>
<td>Sent when the current selection has changed. A <a href="https://msdn.microsoft.com/en-us/library/Bb787952(v=VS.85).aspx">SELCHANGE</a> data structure is also sent, which indicates the new selection range at the type of data the selection is currently over. Controlled through the <a href="https://msdn.microsoft.com/en-us/library/Bb774366(v=VS.85).aspx">ENM_SELCHANGE</a> mask.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb761685(v=VS.85).aspx">EN_SETFOCUS</a>
</td>
<td>Sent when the edit control receives the keyboard focus. No extra data is sent; there is no mask.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb787989(v=VS.85).aspx">EN_STOPNOUNDO</a>
</td>
<td>Sent when an action occurs for which the control cannot allocate enough memory to maintain the undo state. If S_FALSE is returned, the action will be stopped; otherwise, the action will continue.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb761687(v=VS.85).aspx">EN_UPDATE</a>
</td>
<td>Sent before an edit control requests a redraw of altered data or text. No additional data is sent. This event is controlled through the <a href="https://msdn.microsoft.com/en-us/library/Bb774366(v=VS.85).aspx">ENM_UPDATE</a> mask. 
							<b>Rich Edit 2.0 and later:</b> The <a href="https://msdn.microsoft.com/en-us/library/Bb774366(v=VS.85).aspx">ENM_UPDATE</a> mask is ignored and the <a href="https://msdn.microsoft.com/en-us/library/Bb761687(v=VS.85).aspx">EN_UPDATE</a> notification code is always sent. However, when Microsoft Rich Edit 3.0 emulates Microsoft Rich Edit 1.0, the <b>ENM_UPDATE</b> mask controls this notification.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb761689(v=VS.85).aspx">EN_VSCROLL</a>
</td>
<td>Sent when the user clicks an edit control's vertical scroll bar or when the user scrolls the mouse wheel over the edit control, before the screen is updated. This is controlled through the <a href="https://msdn.microsoft.com/en-us/library/Bb774366(v=VS.85).aspx">ENM_SCROLL</a> mask; no extra data is sent.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/en-us/library/Bb787974(v=VS.85).aspx">EN_MSGFILTER</a> is not sent to <b>TxNotify</b>. To filter window messages, use <a href="https://msdn.microsoft.com/en-us/library/Bb787680(v=VS.85).aspx">TxSendMessage</a>.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774238(v=VS.85).aspx">EM_SETEVENTMASK</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761676(v=VS.85).aspx">EN_CHANGE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787966(v=VS.85).aspx">EN_DROPFILES</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761678(v=VS.85).aspx">EN_ERRSPACE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761680(v=VS.85).aspx">EN_HSCROLL</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761682(v=VS.85).aspx">EN_KILLFOCUS</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787970(v=VS.85).aspx">EN_LINK</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761684(v=VS.85).aspx">EN_MAXTEXT</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787979(v=VS.85).aspx">EN_OLEOPFAILED</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787981(v=VS.85).aspx">EN_PROTECTED</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787983(v=VS.85).aspx">EN_REQUESTRESIZE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787985(v=VS.85).aspx">EN_SAVECLIPBOARD</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787987(v=VS.85).aspx">EN_SELCHANGE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761685(v=VS.85).aspx">EN_SETFOCUS</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787989(v=VS.85).aspx">EN_STOPNOUNDO</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761687(v=VS.85).aspx">EN_UPDATE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761689(v=VS.85).aspx">EN_VSCROLL</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls</a>
 

 

