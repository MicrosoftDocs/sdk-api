---
UID: NF:shobjidl_core.IShellView.Refresh
title: IShellView::Refresh (shobjidl_core.h)
description: Refreshes the view's contents in response to user input.
helpviewer_keywords: ["IShellView interface [Windows Shell]","Refresh method","IShellView.Refresh","IShellView::Refresh","Refresh","Refresh method [Windows Shell]","Refresh method [Windows Shell]","IShellView interface","_win32_IShellView_Refresh","shell.IShellView_Refresh","shobjidl_core/IShellView::Refresh"]
old-location: shell\IShellView_Refresh.htm
tech.root: shell
ms.assetid: 510aea71-5885-4d23-8fe9-1fef4881cb18
ms.date: 12/05/2018
ms.keywords: IShellView interface [Windows Shell],Refresh method, IShellView.Refresh, IShellView::Refresh, Refresh, Refresh method [Windows Shell], Refresh method [Windows Shell],IShellView interface, _win32_IShellView_Refresh, shell.IShellView_Refresh, shobjidl_core/IShellView::Refresh
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
 - IShellView::Refresh
 - shobjidl_core/IShellView::Refresh
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
 - IShellView.Refresh
---

# IShellView::Refresh


## -description

Refreshes the view's contents in response to user input.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -remarks

Tells the view to refresh its contents, revalidating any view information it has.

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
Windows Explorer calls this method when the F5 key is pressed on an already open view.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Refill the view by going to any underlying storage for the contents.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>
