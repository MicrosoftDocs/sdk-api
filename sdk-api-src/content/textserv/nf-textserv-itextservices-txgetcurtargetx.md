---
UID: NF:textserv.ITextServices.TxGetCurTargetX
title: ITextServices::TxGetCurTargetX (textserv.h)
description: Gets the target x position, that is, the current horizontal position of the caret.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","TxGetCurTargetX method","ITextServices.TxGetCurTargetX","ITextServices::TxGetCurTargetX","TxGetCurTargetX","TxGetCurTargetX method [Windows Controls]","TxGetCurTargetX method [Windows Controls]","ITextServices interface","_win32_ITextServices_TxGetCurTargetX","_win32_ITextServices_TxGetCurTargetX_cpp","controls.ITextServices_TxGetCurTargetX","controls._win32_ITextServices_TxGetCurTargetX","textserv/ITextServices::TxGetCurTargetX"]
old-location: controls\ITextServices_TxGetCurTargetX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetcurtargetx.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetCurTargetX method, ITextServices.TxGetCurTargetX, ITextServices::TxGetCurTargetX, TxGetCurTargetX, TxGetCurTargetX method [Windows Controls], TxGetCurTargetX method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetCurTargetX, _win32_ITextServices_TxGetCurTargetX_cpp, controls.ITextServices_TxGetCurTargetX, controls._win32_ITextServices_TxGetCurTargetX, textserv/ITextServices::TxGetCurTargetX
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
 - ITextServices::TxGetCurTargetX
 - textserv/ITextServices::TxGetCurTargetX
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
 - ITextServices.TxGetCurTargetX
---

# ITextServices::TxGetCurTargetX


## -description

Gets the target x position, that is, the current horizontal position of the caret.

## -parameters

#### - px

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The target x location in client coordinates.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the x position of the caret is returned, the return value is <b>S_OK</b>.

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
There is no selection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The input argument is invalid.

</td>
</tr>
</table>

## -remarks

Together with <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxsetcursor">ITextServices::OnTxSetCursor</a>, this method allows you to maintain the horizontal caret position when moving the caret up and down. This capability is useful when moving the caret through forms.

The target caret position is expressed as an x-coordinate on the display because other controls do not necessarily share the same attributes for column position.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxsetcursor">OnTxSetCursor</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>