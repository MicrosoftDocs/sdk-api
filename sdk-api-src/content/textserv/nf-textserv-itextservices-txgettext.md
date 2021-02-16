---
UID: NF:textserv.ITextServices.TxGetText
title: ITextServices::TxGetText (textserv.h)
description: Returns all of the Unicode plain text in the control as a BSTR.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","TxGetText method","ITextServices.TxGetText","ITextServices::TxGetText","TxGetText","TxGetText method [Windows Controls]","TxGetText method [Windows Controls]","ITextServices interface","_win32_ITextServices_TxGetText","_win32_ITextServices_TxGetText_cpp","controls.ITextServices_TxGetText","controls._win32_ITextServices_TxGetText","textserv/ITextServices::TxGetText"]
old-location: controls\ITextServices_TxGetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgettext.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetText method, ITextServices.TxGetText, ITextServices::TxGetText, TxGetText, TxGetText method [Windows Controls], TxGetText method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetText, _win32_ITextServices_TxGetText_cpp, controls.ITextServices_TxGetText, controls._win32_ITextServices_TxGetText, textserv/ITextServices::TxGetText
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
 - ITextServices::TxGetText
 - textserv/ITextServices::TxGetText
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
 - ITextServices.TxGetText
---

# ITextServices::TxGetText


## -description

Returns all of the Unicode plain text in the control as a <b>BSTR</b>.

## -parameters

### -param pbstrText

Type: <b>BSTR
          *</b>

The Unicode plain text.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the text is successfully returned in the output argument, the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following <b>HRESULT</b> codes. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid <b>BSTR</b> pointer passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not allocate memory for copy of the text.

</td>
</tr>
</table>

## -remarks

The host (caller) takes ownership of the returned <b>BSTR</b>.

Other ways to retrieve plain text data are to use <a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a> or the Text Object Model (TOM) <a href="/windows/desktop/api/tom/nf-tom-itextrange-gettext">GetText</a> method.

If there is no text in the control, the <b>BSTR</b> is allocated and 0x000D is returned in it.

The returned text will <i>not</i> necessarily be null-terminated.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-gettext">GetText</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>