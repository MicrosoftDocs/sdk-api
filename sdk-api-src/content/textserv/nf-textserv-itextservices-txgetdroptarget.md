---
UID: NF:textserv.ITextServices.TxGetDropTarget
title: ITextServices::TxGetDropTarget (textserv.h)
description: Gets the drop target for the text control.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","TxGetDropTarget method","ITextServices.TxGetDropTarget","ITextServices::TxGetDropTarget","TxGetDropTarget","TxGetDropTarget method [Windows Controls]","TxGetDropTarget method [Windows Controls]","ITextServices interface","_win32_ITextServices_TxGetDropTarget","_win32_ITextServices_TxGetDropTarget_cpp","controls.ITextServices_TxGetDropTarget","controls._win32_ITextServices_TxGetDropTarget","textserv/ITextServices::TxGetDropTarget"]
old-location: controls\ITextServices_TxGetDropTarget.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetdroptarget.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetDropTarget method, ITextServices.TxGetDropTarget, ITextServices::TxGetDropTarget, TxGetDropTarget, TxGetDropTarget method [Windows Controls], TxGetDropTarget method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetDropTarget, _win32_ITextServices_TxGetDropTarget_cpp, controls.ITextServices_TxGetDropTarget, controls._win32_ITextServices_TxGetDropTarget, textserv/ITextServices::TxGetDropTarget
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
 - ITextServices::TxGetDropTarget
 - textserv/ITextServices::TxGetDropTarget
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
 - ITextServices.TxGetDropTarget
---

# ITextServices::TxGetDropTarget


## -description

Gets the drop target for the text control.

## -parameters

### -param ppDropTarget

Type: <b><a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>**</b>

The target of a drag-and-drop operation in a specified window.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method got the drop target successfully, the return value is <b>S_OK</b>.

 For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
Could not create the drop target.

</td>
</tr>
</table>

## -remarks

The host (caller) is responsible for calling <a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a> or <a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a>, and for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the returned drop target when done.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a>



<a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>