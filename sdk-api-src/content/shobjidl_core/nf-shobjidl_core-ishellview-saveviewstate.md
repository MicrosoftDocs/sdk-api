---
UID: NF:shobjidl_core.IShellView.SaveViewState
title: IShellView::SaveViewState (shobjidl_core.h)
description: Saves the Shell's view settings so the current state can be restored during a subsequent browsing session.
helpviewer_keywords: ["IShellView interface [Windows Shell]","SaveViewState method","IShellView.SaveViewState","IShellView::SaveViewState","SaveViewState","SaveViewState method [Windows Shell]","SaveViewState method [Windows Shell]","IShellView interface","_win32_IShellView_SaveViewState","shell.IShellView_SaveViewState","shobjidl_core/IShellView::SaveViewState"]
old-location: shell\IShellView_SaveViewState.htm
tech.root: shell
ms.assetid: 4bc36340-1e52-48cf-8b9a-e32115cda88b
ms.date: 12/05/2018
ms.keywords: IShellView interface [Windows Shell],SaveViewState method, IShellView.SaveViewState, IShellView::SaveViewState, SaveViewState, SaveViewState method [Windows Shell], SaveViewState method [Windows Shell],IShellView interface, _win32_IShellView_SaveViewState, shell.IShellView_SaveViewState, shobjidl_core/IShellView::SaveViewState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellView::SaveViewState
 - shobjidl_core/IShellView::SaveViewState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellView.SaveViewState
---

# IShellView::SaveViewState


## -description

Saves the Shell's view settings so the current state can be restored during a subsequent browsing session.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -remarks

The Shell view obtains a view stream by calling the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream">GetViewStateStream</a> method and stores the current view state in that stream.

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
Windows Explorer calls this method when it wants to save the view state for a view.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Be sure to make the format of the data stored in the stream robust enough that different versions of the implementation can read it without error.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>
