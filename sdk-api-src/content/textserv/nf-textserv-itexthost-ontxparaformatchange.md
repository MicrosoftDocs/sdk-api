---
UID: NF:textserv.ITextHost.OnTxParaFormatChange
title: ITextHost::OnTxParaFormatChange (textserv.h)
description: Sets the default paragraph format for the text host.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","OnTxParaFormatChange method","ITextHost.OnTxParaFormatChange","ITextHost::OnTxParaFormatChange","OnTxParaFormatChange","OnTxParaFormatChange method [Windows Controls]","OnTxParaFormatChange method [Windows Controls]","ITextHost interface","_win32_ITextHost_OnTxParaFormatChange","_win32_ITextHost_OnTxParaFormatChange_cpp","controls.ITextHost_OnTxParaFormatChange","controls._win32_ITextHost_OnTxParaFormatChange","textserv/ITextHost::OnTxParaFormatChange"]
old-location: controls\ITextHost_OnTxParaFormatChange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxparaformatchange.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],OnTxParaFormatChange method, ITextHost.OnTxParaFormatChange, ITextHost::OnTxParaFormatChange, OnTxParaFormatChange, OnTxParaFormatChange method [Windows Controls], OnTxParaFormatChange method [Windows Controls],ITextHost interface, _win32_ITextHost_OnTxParaFormatChange, _win32_ITextHost_OnTxParaFormatChange_cpp, controls.ITextHost_OnTxParaFormatChange, controls._win32_ITextHost_OnTxParaFormatChange, textserv/ITextHost::OnTxParaFormatChange
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
 - ITextHost::OnTxParaFormatChange
 - textserv/ITextHost::OnTxParaFormatChange
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
 - ITextHost.OnTxParaFormatChange
---

# ITextHost::OnTxParaFormatChange


## -description

Sets the default paragraph format for the text host.

## -parameters

### -param pPF [in]

Type: <b>const <a href="/windows/desktop/api/richedit/ns-richedit-paraformat">PARAFORMAT</a>*</b>

The new default paragraph format.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Return S_OK if the method succeeds. 

Return one of the following COM error codes if the method fails. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>. 

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
One or more arguments are not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/api/richedit/ns-richedit-paraformat">PARAFORMAT</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>