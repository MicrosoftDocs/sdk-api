---
UID: NF:textserv.ITextServices.TxSetText
title: ITextServices::TxSetText (textserv.h)
description: Sets all of the text in the control.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","TxSetText method","ITextServices.TxSetText","ITextServices::TxSetText","TxSetText","TxSetText method [Windows Controls]","TxSetText method [Windows Controls]","ITextServices interface","_win32_ITextServices_TxSetText","_win32_ITextServices_TxSetText_cpp","controls.ITextServices_TxSetText","controls._win32_ITextServices_TxSetText","textserv/ITextServices::TxSetText"]
old-location: controls\ITextServices_TxSetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsettext.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],TxSetText method, ITextServices.TxSetText, ITextServices::TxSetText, TxSetText, TxSetText method [Windows Controls], TxSetText method [Windows Controls],ITextServices interface, _win32_ITextServices_TxSetText, _win32_ITextServices_TxSetText_cpp, controls.ITextServices_TxSetText, controls._win32_ITextServices_TxSetText, textserv/ITextServices::TxSetText
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
 - ITextServices::TxSetText
 - textserv/ITextServices::TxSetText
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
 - ITextServices.TxSetText
---

# ITextServices::TxSetText


## -description

Sets all of the text in the control.

## -parameters

### -param pszText [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The string which will replace the current text.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, the return value is <b>S_OK</b>.

If the method fails, the return value is the following <b>HRESULT</b> code. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Text could not be updated.

</td>
</tr>
</table>

## -remarks

This method should be used with care; it essentially reinitializes the text services object with some new data. Any previous data and formatting information will be lost, including undo information.

If previous data has been copied to the clipboard, that data will be rendered completely to the clipboard (through <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a>) before it is discarded.

This method does <i>not</i> support <b>Undo</b>.

Two alternate approaches to setting text are <a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-settext">SetText</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-settext">SetText</a>



<a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>