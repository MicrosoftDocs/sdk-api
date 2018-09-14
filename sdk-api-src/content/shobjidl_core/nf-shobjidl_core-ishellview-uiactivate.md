---
UID: NF:shobjidl_core.IShellView.UIActivate
title: IShellView::UIActivate
author: windows-sdk-content
description: Called when the activation state of the view window is changed by an event that is not caused by the Shell view itself. For example, if the TAB key is pressed when the tree has the focus, the view should be given the focus.
old-location: shell\IShellView_UIActivate.htm
tech.root: shell
ms.assetid: 169881de-d073-4864-beb2-4e030b855e8f
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IShellView interface [Windows Shell],UIActivate method, IShellView.UIActivate, IShellView::UIActivate, SVUIA_ACTIVATE_FOCUS, SVUIA_ACTIVATE_NOFOCUS, SVUIA_DEACTIVATE, SVUIA_INPLACEACTIVATE, UIActivate, UIActivate method [Windows Shell], UIActivate method [Windows Shell],IShellView interface, _win32_IShellView_UIActivate, shell.IShellView_UIActivate, shobjidl_core/IShellView::UIActivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellView.UIActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellView::UIActivate


## -description


Called when the activation state of the view window is changed by an event that is not caused by the Shell view itself. For example, if the TAB key is pressed when the tree has the focus, the view should be given the focus.


## -parameters




### -param uState

Type: <b>UINT</b>

Flag specifying the activation state of the window. This parameter can be one of the following values.



#### SVUIA_ACTIVATE_FOCUS

Windows Explorer has just created the view window with the input focus. This means the Shell view should be able to set menu items appropriate for the focused state.



#### SVUIA_ACTIVATE_NOFOCUS

The Shell view is losing the input focus, or it has just been created without the input focus. The Shell view should be able to set menu items appropriate for the nonfocused state. This means no selection-specific items should be added.



#### SVUIA_DEACTIVATE

Windows Explorer is about to destroy the Shell view window. The Shell view should remove all extended user interfaces. These are typically merged menus and merged modeless pop-up windows.



#### SVUIA_INPLACEACTIVATE

The Shell view is active without focus. This flag is only used when <b>UIActivate</b> is exposed through the <a href="https://msdn.microsoft.com/a61aec39-406d-4066-941d-e788d64f4310">IShellView2</a> interface.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a COM-defined error value otherwise.




## -remarks



Before remerging menu items, the Shell view typically hooks the <a href="https://msdn.microsoft.com/77180e4c-95a6-41a4-93d9-033381ae7543">WM_SETFOCUS</a> message and calls the <a href="https://msdn.microsoft.com/bd320262-f383-453b-9028-4e93f0b3761a">OnViewWindowActive</a> method. The Shell view should not hook the <a href="https://msdn.microsoft.com/d7538697-8b4c-4bbd-8b06-02cbc8069a22">NM_KILLFOCUS</a> message to remerge menu items.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
Call this method to inform the view of an activation state change.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Use this method to track the activation state and change any behavior, as appropriate.




## -see-also




<a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>
 

 

