---
UID: NF:richole.IRichEditOleCallback.GetDragDropEffect
title: IRichEditOleCallback::GetDragDropEffect
author: windows-sdk-content
description: Allows the client to specify the effects of a drop operation.
old-location: controls\IRichEditOleCallback_GetDragDropEffect.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackgetdragdropeffect.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetDragDropEffect, GetDragDropEffect method [Windows Controls], GetDragDropEffect method [Windows Controls],IRichEditOleCallback interface, IRichEditOleCallback interface [Windows Controls],GetDragDropEffect method, IRichEditOleCallback.GetDragDropEffect, IRichEditOleCallback::GetDragDropEffect, _win32_IRichEditOleCallback_GetDragDropEffect, _win32_IRichEditOleCallback_GetDragDropEffect_cpp, controls.IRichEditOleCallback_GetDragDropEffect, controls._win32_IRichEditOleCallback_GetDragDropEffect, richole/IRichEditOleCallback::GetDragDropEffect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOleCallback.GetDragDropEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- richole.h
: 
- IRichEditOleCallback.GetDragDropEffect
: 
---

# IRichEditOleCallback::GetDragDropEffect


## -description


Allows the client to specify the effects of a drop operation.


## -parameters




### -param fDrag

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the query is for a <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a> or <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a>. <b>FALSE</b> if the query is for <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a>. 


### -param grfKeyState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Key state as defined by OLE.


### -param pdwEffect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPDWORD</a></b>

The effect used by a rich edit control. When 
					<i>fDrag</i> is <b>TRUE</b>, on return, its content is set to the effect allowable by the rich edit control. When 
					<i>fDrag</i> is <b>FALSE</b>, on return, the variable is set to the effect to use. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

This method returns <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774308(v=VS.85).aspx">IRichEditOleCallback</a>
 

 

