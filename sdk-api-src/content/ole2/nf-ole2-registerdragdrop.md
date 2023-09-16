---
UID: NF:ole2.RegisterDragDrop
title: RegisterDragDrop function (ole2.h)
description: Registers the specified window as one that can be the target of an OLE drag-and-drop operation and specifies the IDropTarget instance to use for drop operations.
helpviewer_keywords: ["RegisterDragDrop","RegisterDragDrop function [COM]","_ole_RegisterDragDrop","com.registerdragdrop","ole2/RegisterDragDrop"]
old-location: com\registerdragdrop.htm
tech.root: com
ms.assetid: 00726271-4436-41f5-b7cc-666cd77216bc
ms.date: 12/05/2018
ms.keywords: RegisterDragDrop, RegisterDragDrop function [COM], _ole_RegisterDragDrop, com.registerdragdrop, ole2/RegisterDragDrop
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterDragDrop
 - ole2/RegisterDragDrop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - RegisterDragDrop
---

# RegisterDragDrop function


## -description

Registers the specified window as one that can be the target of an OLE drag-and-drop operation and specifies the <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> instance to use for drop operations.

## -parameters

### -param hwnd [in]

Handle to a window that can be a target for an OLE drag-and-drop operation.

### -param pDropTarget [in]

Pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface on the object that is to be the target of a drag-and-drop operation in a specified window. This interface is used to communicate OLE drag-and-drop information for that window.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_E_INVALIDHWND</b></dt>
</dl>
</td>
<td width="60%">
Invalid handle returned in the hwnd parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_E_ALREADYREGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The specified window has already been registered as a drop target.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If you use <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> instead of <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> to initialize COM, <b>RegisterDragDrop</b> will always return an E_OUTOFMEMORY error.</div>
<div> </div>

## -remarks

If your application can accept dropped objects during OLE drag-and-drop operations, you must call the <b>RegisterDragDrop</b> function. Do this whenever one of your application windows is available as a potential drop target, i.e., when the window appears unobscured on the screen.

The application thread that calls the <b>RegisterDragDrop</b> function must be pumping messages, presumably by calling the <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> function with a <b>NULL</b> <i>hWnd</i> parameter, because OLE creates windows on the thread that need messages processed. If this requirement is not met, any application that drags an object over the window that is registered as a drop target will hang until the target application closes.

The <b>RegisterDragDrop</b> function only registers one window at a time, so you must call it for each application window capable of accepting dropped objects.

As the mouse passes over unobscured portions of the target window during an OLE drag-and-drop operation, the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function calls the specified <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a> method for the current window. When a drop operation actually occurs in a given window, the <b>DoDragDrop</b> function calls <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a>.

The <b>RegisterDragDrop</b> function also calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> method on the <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> pointer.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a>
