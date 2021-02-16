---
UID: NF:textserv.ITextHost.TxActivate
title: ITextHost::TxActivate (textserv.h)
description: Notifies the text host that the control is active.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxActivate method","ITextHost.TxActivate","ITextHost::TxActivate","TxActivate","TxActivate method [Windows Controls]","TxActivate method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxActivate","_win32_ITextHost_TxActivate_cpp","controls.ITextHost_TxActivate","controls._win32_ITextHost_TxActivate","textserv/ITextHost::TxActivate"]
old-location: controls\ITextHost_TxActivate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txactivate.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxActivate method, ITextHost.TxActivate, ITextHost::TxActivate, TxActivate, TxActivate method [Windows Controls], TxActivate method [Windows Controls],ITextHost interface, _win32_ITextHost_TxActivate, _win32_ITextHost_TxActivate_cpp, controls.ITextHost_TxActivate, controls._win32_ITextHost_TxActivate, textserv/ITextHost::TxActivate
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
 - ITextHost::TxActivate
 - textserv/ITextHost::TxActivate
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
 - ITextHost.TxActivate
---

# ITextHost::TxActivate


## -description

Notifies the text host that the control is active.

## -parameters

### -param plOldState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The previous activation state.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Activation is not possible at this time.

</td>
</tr>
</table>

## -remarks

It is legal for the host to refuse an activation request; for example, the control may be minimized and thus invisible.

The caller should be able to gracefully handle failure to activate.

No matter how many times this method is called, only one <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txdeactivate">ITextHost::TxDeactivate</a> call is necessary to deactivate the control.

This function returns an opaque handle in 
				<i>plOldState</i>. The caller (the text services object) should save this handle and use it in a subsequent call to <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txdeactivate">ITextHost::TxDeactivate</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txdeactivate">TxDeactivate</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>