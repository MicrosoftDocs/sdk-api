---
UID: NF:shobjidl_core.IShellView.SaveViewState
title: IShellView::SaveViewState
author: windows-sdk-content
description: Saves the Shell's view settings so the current state can be restored during a subsequent browsing session.
old-location: shell\IShellView_SaveViewState.htm
tech.root: shell
ms.assetid: 4bc36340-1e52-48cf-8b9a-e32115cda88b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellView interface [Windows Shell],SaveViewState method, IShellView.SaveViewState, IShellView::SaveViewState, SaveViewState, SaveViewState method [Windows Shell], SaveViewState method [Windows Shell],IShellView interface, _win32_IShellView_SaveViewState, shell.IShellView_SaveViewState, shobjidl_core/IShellView::SaveViewState
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
 - IShellView.SaveViewState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellView::SaveViewState


## -description


Saves the Shell's view settings so the current state can be restored during a subsequent browsing session.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.




## -remarks



The Shell view obtains a view stream by calling the <a href="https://msdn.microsoft.com/887ebe9f-8bde-46dd-a7a2-7b2ca66bf905">GetViewStateStream</a> method and stores the current view state in that stream.

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
Windows Explorer calls this method when it wants to save the view state for a view.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Be sure to make the format of the data stored in the stream robust enough that different versions of the implementation can read it without error.




## -see-also




<a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>
 

 

