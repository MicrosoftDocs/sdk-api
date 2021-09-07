---
UID: NF:shobjidl_core.ICommDlgBrowser.OnStateChange
title: ICommDlgBrowser::OnStateChange (shobjidl_core.h)
description: Called after a state, identified by the uChange parameter, has changed in the IShellView interface.
helpviewer_keywords: ["CDBOSC_KILLFOCUS","CDBOSC_RENAME","CDBOSC_SELCHANGE","CDBOSC_SETFOCUS","CDBOSC_STATECHANGE","ICommDlgBrowser interface [Windows Shell]","OnStateChange method","ICommDlgBrowser.OnStateChange","ICommDlgBrowser::OnStateChange","OnStateChange","OnStateChange method [Windows Shell]","OnStateChange method [Windows Shell]","ICommDlgBrowser interface","_win32_ICommDlgBrowser_OnStateChange","shell.ICommDlgBrowser_OnStateChange","shobjidl_core/ICommDlgBrowser::OnStateChange"]
old-location: shell\ICommDlgBrowser_OnStateChange.htm
tech.root: shell
ms.assetid: ec9f0e5d-ca64-4ab4-b2cc-6d0748ede8b2
ms.date: 12/05/2018
ms.keywords: CDBOSC_KILLFOCUS, CDBOSC_RENAME, CDBOSC_SELCHANGE, CDBOSC_SETFOCUS, CDBOSC_STATECHANGE, ICommDlgBrowser interface [Windows Shell],OnStateChange method, ICommDlgBrowser.OnStateChange, ICommDlgBrowser::OnStateChange, OnStateChange, OnStateChange method [Windows Shell], OnStateChange method [Windows Shell],ICommDlgBrowser interface, _win32_ICommDlgBrowser_OnStateChange, shell.ICommDlgBrowser_OnStateChange, shobjidl_core/ICommDlgBrowser::OnStateChange
req.header: shobjidl_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICommDlgBrowser::OnStateChange
 - shobjidl_core/ICommDlgBrowser::OnStateChange
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
 - ICommDlgBrowser.OnStateChange
---

# ICommDlgBrowser::OnStateChange


## -description

Called after a state, identified by the <i>uChange</i> parameter, has changed in the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.

## -parameters

### -param ppshv

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the view's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.

### -param uChange

Type: <b>ULONG</b>

Change in the selection state. This parameter can be one of the following values.



#### CDBOSC_SETFOCUS

The focus has been set to the view.



#### CDBOSC_KILLFOCUS

The view has lost the focus.



#### CDBOSC_SELCHANGE

The selection has changed.



#### CDBOSC_RENAME

An item has been renamed.



#### CDBOSC_STATECHANGE

An item has been checked or unchecked.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used to let the common file dialog boxes track the state of the view and change its user interface as needed.

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
When items in the view are selected, or when the view loses the focus, it needs to call this method to notify the common dialog that either the view state or selection state is changing.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a>