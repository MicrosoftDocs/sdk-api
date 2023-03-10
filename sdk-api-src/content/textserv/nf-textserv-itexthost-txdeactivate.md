---
UID: NF:textserv.ITextHost.TxDeactivate
title: ITextHost::TxDeactivate (textserv.h)
description: Notifies the text host that the control is now inactive.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxDeactivate method","ITextHost.TxDeactivate","ITextHost::TxDeactivate","TxDeactivate","TxDeactivate method [Windows Controls]","TxDeactivate method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxDeactivate","_win32_ITextHost_TxDeactivate_cpp","controls.ITextHost_TxDeactivate","controls._win32_ITextHost_TxDeactivate","textserv/ITextHost::TxDeactivate"]
old-location: controls\ITextHost_TxDeactivate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txdeactivate.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxDeactivate method, ITextHost.TxDeactivate, ITextHost::TxDeactivate, TxDeactivate, TxDeactivate method [Windows Controls], TxDeactivate method [Windows Controls],ITextHost interface, _win32_ITextHost_TxDeactivate, _win32_ITextHost_TxDeactivate_cpp, controls.ITextHost_TxDeactivate, controls._win32_ITextHost_TxDeactivate, textserv/ITextHost::TxDeactivate
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
 - ITextHost::TxDeactivate
 - textserv/ITextHost::TxDeactivate
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
 - ITextHost.TxDeactivate
---

# ITextHost::TxDeactivate


## -description

Notifies the text host that the control is now inactive.

## -parameters

### -param lNewState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

New state of the control. Typically it is the value returned by <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txactivate">ITextHost::TxActivate</a>.

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
Unspecified error.

</td>
</tr>
</table>

## -remarks

No matter how many times this method is called, only one call to <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txactivate">ITextHost::TxActivate</a> is necessary to activate the control.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txactivate">TxActivate</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>