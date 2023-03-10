---
UID: NF:shobjidl_core.IShellView.TranslateAccelerator
title: IShellView::TranslateAccelerator (shobjidl_core.h)
description: Translates keyboard shortcut (accelerator) key strokes when a namespace extension's view has the focus.
helpviewer_keywords: ["IShellView interface [Windows Shell]","TranslateAccelerator method","IShellView.TranslateAccelerator","IShellView::TranslateAccelerator","TranslateAccelerator","TranslateAccelerator method [Windows Shell]","TranslateAccelerator method [Windows Shell]","IShellView interface","_win32_IShellView_TranslateAccelerator","shell.IShellView_TranslateAccelerator","shobjidl_core/IShellView::TranslateAccelerator"]
old-location: shell\IShellView_TranslateAccelerator.htm
tech.root: shell
ms.assetid: 425a281e-2d34-4bb3-92b9-05ae4cf70a9f
ms.date: 12/05/2018
ms.keywords: IShellView interface [Windows Shell],TranslateAccelerator method, IShellView.TranslateAccelerator, IShellView::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [Windows Shell], TranslateAccelerator method [Windows Shell],IShellView interface, _win32_IShellView_TranslateAccelerator, shell.IShellView_TranslateAccelerator, shobjidl_core/IShellView::TranslateAccelerator
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
 - IShellView::TranslateAccelerator
 - shobjidl_core/IShellView::TranslateAccelerator
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
 - IShellView.TranslateAccelerator
---

# IShellView::TranslateAccelerator


## -description

Translates keyboard shortcut (accelerator) key strokes when a namespace extension's view has the focus.

## -parameters

### -param pmsg

Type: <b>LPMSG</b>

The address of the message to be translated.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

If the view returns S_OK, it indicates that the message was translated and should not be translated or dispatched by Windows Explorer.

## -remarks

This method is called by Windows Explorer to let the view translate its keyboard shortcuts.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
Windows Explorer calls this method before any other translation if the view has the focus. If the view does not have the focus, it is called after Windows Explorer translates its own keyboard shortcuts.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
By default, the view should return S_FALSE so that Windows Explorer can either do its own keyboard shortcut translation or normal menu dispatching. The view should return S_OK only if it has processed the message as the keyboard shortcut and does not want Windows Explorer to process it further.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>