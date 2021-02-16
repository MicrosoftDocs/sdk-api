---
UID: NF:textserv.ITextServices.TxSendMessage
title: ITextServices::TxSendMessage (textserv.h)
description: Used by the window host to forward messages sent from its window to the text services object.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","TxSendMessage method","ITextServices.TxSendMessage","ITextServices::TxSendMessage","TxSendMessage","TxSendMessage method [Windows Controls]","TxSendMessage method [Windows Controls]","ITextServices interface","_win32_ITextServices_TxSendMessage","_win32_ITextServices_TxSendMessage_cpp","controls.ITextServices_TxSendMessage","controls._win32_ITextServices_TxSendMessage","textserv/ITextServices::TxSendMessage"]
old-location: controls\ITextServices_TxSendMessage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsendmessage.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],TxSendMessage method, ITextServices.TxSendMessage, ITextServices::TxSendMessage, TxSendMessage, TxSendMessage method [Windows Controls], TxSendMessage method [Windows Controls],ITextServices interface, _win32_ITextServices_TxSendMessage, _win32_ITextServices_TxSendMessage_cpp, controls.ITextServices_TxSendMessage, controls._win32_ITextServices_TxSendMessage, textserv/ITextServices::TxSendMessage
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
 - ITextServices::TxSendMessage
 - textserv/ITextServices::TxSendMessage
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
 - ITextServices.TxSendMessage
---

# ITextServices::TxSendMessage


## -description

Used by the window host to forward messages sent from its window to the text services object.

## -parameters

### -param msg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The message identifier.

### -param wparam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WPARAM</a></b>

The <b>WPARAM</b> from the window's message.

### -param lparam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The <b>LPARAM</b> from the window's message.

### -param plresult

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LRESULT</a>*</b>

The message's return <b>LRESULT</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following <b>HRESULT</b> codes. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory. NOERROR Message was processed, and some action was taken. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Message was not processed. Typically indicates that the caller should process the message itself, potentially by calling <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_MSG_KEYIGNORED</b></dt>
</dl>
</td>
<td width="60%">
Message processed, but no action was taken for the keystroke. 

</td>
</tr>
</table>

## -remarks

Note that two return values are passed back from this function. The return value that should be passed back from a window procedure is <i>plresult</i>. However, in some cases, the returned <b>LRESULT</b> does not contain enough information. For example, to implement moving the cursor around controls, it's useful to know if a keystroke (such as right arrow) was processed but ignored (for example, the caret is already at the rightmost position in the text). In these cases, more information may be returned through the returned <b>HRESULT</b>.


<a href="/windows/desktop/inputdev/wm-char">WM_CHAR</a> and <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> should return the value S_MSG_KEYIGNORED when a key or character is recognized, but has no effect, given the current state. For example, S_MSG_KEYIGNORED should be returned in the following cases: 
				

<ul>
<li>Any keystroke that tries to move the insertion point to or beyond the beginning or the end of the document; when it is already at the beginning or end of the document, respectively. </li>
<li>Any keystroke that tries to move the insertion point to or past the next line when it is already on the last line; or to or before the previous line when it is already on the first line. </li>
<li>Any insertion of the character from <a href="/windows/desktop/inputdev/wm-char">WM_CHAR</a> that would move the insertion point past the maximum length of the control. </li>
</ul>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<b>Other Resources</b>



<a href="/windows/desktop/inputdev/wm-char">WM_CHAR</a>



<a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>