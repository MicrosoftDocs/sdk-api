---
UID: NF:textserv.ITextHost.TxGetParaFormat
title: ITextHost::TxGetParaFormat (textserv.h)
description: Requests the text host's default paragraph format.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetParaFormat method","ITextHost.TxGetParaFormat","ITextHost::TxGetParaFormat","TxGetParaFormat","TxGetParaFormat method [Windows Controls]","TxGetParaFormat method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetParaFormat","_win32_ITextHost_TxGetParaFormat_cpp","controls.ITextHost_TxGetParaFormat","controls._win32_ITextHost_TxGetParaFormat","textserv/ITextHost::TxGetParaFormat"]
old-location: controls\ITextHost_TxGetParaFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetparaformat.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetParaFormat method, ITextHost.TxGetParaFormat, ITextHost::TxGetParaFormat, TxGetParaFormat, TxGetParaFormat method [Windows Controls], TxGetParaFormat method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetParaFormat, _win32_ITextHost_TxGetParaFormat_cpp, controls.ITextHost_TxGetParaFormat, controls._win32_ITextHost_TxGetParaFormat, textserv/ITextHost::TxGetParaFormat
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
 - ITextHost::TxGetParaFormat
 - textserv/ITextHost::TxGetParaFormat
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
 - ITextHost.TxGetParaFormat
---

# ITextHost::TxGetParaFormat


## -description

Requests the text host's default paragraph format.

## -parameters

### -param ppPF

Type: <b>const <a href="/windows/desktop/api/richedit/ns-richedit-paraformat">PARAFORMAT</a>**</b>

The default paragraph format.

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

The host object retains ownership of the <a href="/windows/desktop/api/richedit/ns-richedit-paraformat">PARAFORMAT</a> structure that is returned. However, the pointer returned must remain valid until the host notifies the text services object, through <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a>, that the default paragraph format has changed.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a>



<a href="/windows/desktop/api/richedit/ns-richedit-paraformat">PARAFORMAT</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>