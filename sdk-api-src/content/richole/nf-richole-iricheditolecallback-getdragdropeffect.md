---
UID: NF:richole.IRichEditOleCallback.GetDragDropEffect
title: IRichEditOleCallback::GetDragDropEffect (richole.h)
description: Allows the client to specify the effects of a drop operation.
helpviewer_keywords: ["GetDragDropEffect","GetDragDropEffect method [Windows Controls]","GetDragDropEffect method [Windows Controls]","IRichEditOleCallback interface","IRichEditOleCallback interface [Windows Controls]","GetDragDropEffect method","IRichEditOleCallback.GetDragDropEffect","IRichEditOleCallback::GetDragDropEffect","_win32_IRichEditOleCallback_GetDragDropEffect","_win32_IRichEditOleCallback_GetDragDropEffect_cpp","controls.IRichEditOleCallback_GetDragDropEffect","controls._win32_IRichEditOleCallback_GetDragDropEffect","richole/IRichEditOleCallback::GetDragDropEffect"]
old-location: controls\IRichEditOleCallback_GetDragDropEffect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackgetdragdropeffect.htm
ms.date: 12/05/2018
ms.keywords: GetDragDropEffect, GetDragDropEffect method [Windows Controls], GetDragDropEffect method [Windows Controls],IRichEditOleCallback interface, IRichEditOleCallback interface [Windows Controls],GetDragDropEffect method, IRichEditOleCallback.GetDragDropEffect, IRichEditOleCallback::GetDragDropEffect, _win32_IRichEditOleCallback_GetDragDropEffect, _win32_IRichEditOleCallback_GetDragDropEffect_cpp, controls.IRichEditOleCallback_GetDragDropEffect, controls._win32_IRichEditOleCallback_GetDragDropEffect, richole/IRichEditOleCallback::GetDragDropEffect
req.header: richole.h
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
 - IRichEditOleCallback::GetDragDropEffect
 - richole/IRichEditOleCallback::GetDragDropEffect
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
 - IRichEditOleCallback.GetDragDropEffect
---

# IRichEditOleCallback::GetDragDropEffect


## -description

Allows the client to specify the effects of a drop operation.

## -parameters

### -param fDrag

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the query is for a <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> or <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a>. <b>FALSE</b> if the query is for <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a>.

### -param grfKeyState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Key state as defined by OLE.

### -param pdwEffect

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPDWORD</a></b>

The effect used by a rich edit control. When 
					<i>fDrag</i> is <b>TRUE</b>, on return, its content is set to the effect allowable by the rich edit control. When 
					<i>fDrag</i> is <b>FALSE</b>, on return, the variable is set to the effect to use.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

This method returns <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditolecallback">IRichEditOleCallback</a>