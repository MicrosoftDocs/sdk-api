---
UID: NF:textserv.ITextServices.TxSendMessage
title: ITextServices::TxSendMessage
author: windows-sdk-content
description: Used by the window host to forward messages sent from its window to the text services object.
old-location: controls\ITextServices_TxSendMessage.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsendmessage.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextServices interface [Windows Controls],TxSendMessage method, ITextServices.TxSendMessage, ITextServices::TxSendMessage, TxSendMessage, TxSendMessage method [Windows Controls], TxSendMessage method [Windows Controls],ITextServices interface, _win32_ITextServices_TxSendMessage, _win32_ITextServices_TxSendMessage_cpp, controls.ITextServices_TxSendMessage, controls._win32_ITextServices_TxSendMessage, textserv/ITextServices::TxSendMessage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextServices.TxSendMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextServices::TxSendMessage


## -description


Used by the window host to forward messages sent from its window to the text services object.


## -parameters




### -param msg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The message identifier. 


### -param wparam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WPARAM</a></b>

The <b>WPARAM</b> from the window's message. 


### -param lparam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The <b>LPARAM</b> from the window's message. 


### -param plresult

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LRESULT</a>*</b>

The message's return <b>LRESULT</b>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following <b>HRESULT</b> codes. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
Message was not processed. Typically indicates that the caller should process the message itself, potentially by calling <a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a>. 

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


<a href="https://msdn.microsoft.com/7e45dc6f-ff68-4534-9e52-46e5f4110532">WM_CHAR</a> and <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a> should return the value S_MSG_KEYIGNORED when a key or character is recognized, but has no effect, given the current state. For example, S_MSG_KEYIGNORED should be returned in the following cases: 
				

<ul>
<li>Any keystroke that tries to move the insertion point to or beyond the beginning or the end of the document; when it is already at the beginning or end of the document, respectively. </li>
<li>Any keystroke that tries to move the insertion point to or past the next line when it is already on the last line; or to or before the previous line when it is already on the first line. </li>
<li>Any insertion of the character from <a href="https://msdn.microsoft.com/7e45dc6f-ff68-4534-9e52-46e5f4110532">WM_CHAR</a> that would move the insertion point past the maximum length of the control. </li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/fcc6b242-e152-4364-a977-b0441bec425f">DefWindowProc</a>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/7e45dc6f-ff68-4534-9e52-46e5f4110532">WM_CHAR</a>



<a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

