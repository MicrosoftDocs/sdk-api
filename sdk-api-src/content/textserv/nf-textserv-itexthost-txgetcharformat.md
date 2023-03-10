---
UID: NF:textserv.ITextHost.TxGetCharFormat
title: ITextHost::TxGetCharFormat (textserv.h)
description: Requests the text host's default character format.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetCharFormat method","ITextHost.TxGetCharFormat","ITextHost::TxGetCharFormat","TxGetCharFormat","TxGetCharFormat method [Windows Controls]","TxGetCharFormat method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetCharFormat","_win32_ITextHost_TxGetCharFormat_cpp","controls.ITextHost_TxGetCharFormat","controls._win32_ITextHost_TxGetCharFormat","textserv/ITextHost::TxGetCharFormat"]
old-location: controls\ITextHost_TxGetCharFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetcharformat.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetCharFormat method, ITextHost.TxGetCharFormat, ITextHost::TxGetCharFormat, TxGetCharFormat, TxGetCharFormat method [Windows Controls], TxGetCharFormat method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetCharFormat, _win32_ITextHost_TxGetCharFormat_cpp, controls.ITextHost_TxGetCharFormat, controls._win32_ITextHost_TxGetCharFormat, textserv/ITextHost::TxGetCharFormat
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
 - ITextHost::TxGetCharFormat
 - textserv/ITextHost::TxGetCharFormat
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
 - ITextHost.TxGetCharFormat
---

# ITextHost::TxGetCharFormat


## -description

Requests the text host's default character format.

## -parameters

### -param ppCF

Type: <b>const <a href="/windows/win32/api/richedit/ns-richedit-charformata">CHARFORMAT</a>**</b>

The default character format.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Return S_OK if the method succeeds. 

Return the following COM error code if the method fails. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

## -remarks

The text host retains ownership of the <a href="/windows/win32/api/richedit/ns-richedit-charformata">CHARFORMAT</a> returned. However, the pointer returned must remain valid until the text host notifies the text services object through <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a> that the default character format has changed.

## -see-also

<a href="/windows/win32/api/richedit/ns-richedit-charformata">CHARFORMAT</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>