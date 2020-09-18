---
UID: NF:shobjidl_core.IShellBrowser.GetViewStateStream
title: IShellBrowser::GetViewStateStream (shobjidl_core.h)
description: Gets an IStream interface that can be used for storage of view-specific state information.
helpviewer_keywords: ["GetViewStateStream","GetViewStateStream method [Windows Shell]","GetViewStateStream method [Windows Shell]","IShellBrowser interface","IShellBrowser interface [Windows Shell]","GetViewStateStream method","IShellBrowser.GetViewStateStream","IShellBrowser::GetViewStateStream","STGM_READ","STGM_READWRITE","STGM_WRITE","_win32_IShellBrowser_GetViewStateStream","shell.IShellBrowser_GetViewStateStream","shobjidl_core/IShellBrowser::GetViewStateStream"]
old-location: shell\IShellBrowser_GetViewStateStream.htm
tech.root: shell
ms.assetid: 887ebe9f-8bde-46dd-a7a2-7b2ca66bf905
ms.date: 12/05/2018
ms.keywords: GetViewStateStream, GetViewStateStream method [Windows Shell], GetViewStateStream method [Windows Shell],IShellBrowser interface, IShellBrowser interface [Windows Shell],GetViewStateStream method, IShellBrowser.GetViewStateStream, IShellBrowser::GetViewStateStream, STGM_READ, STGM_READWRITE, STGM_WRITE, _win32_IShellBrowser_GetViewStateStream, shell.IShellBrowser_GetViewStateStream, shobjidl_core/IShellBrowser::GetViewStateStream
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
 - IShellBrowser::GetViewStateStream
 - shobjidl_core/IShellBrowser::GetViewStateStream
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
 - IShellBrowser.GetViewStateStream
---

# IShellBrowser::GetViewStateStream


## -description

Gets an 
			<b>IStream</b> interface that can be used for storage of view-specific state information.

## -parameters

### -param grfMode

Type: <b>DWORD</b>

Read/write access of the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface. This may be one of the following values.



#### STGM_READ

Requests an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> suitable for reading.



#### STGM_WRITE

Requests an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> suitable for writing.



#### STGM_READWRITE

Requests an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> suitable for reading and writing.

### -param ppStrm

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

The address that receives the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -remarks

This method is used to save and restore the persistent state for a view (the icon positions, the column widths, and the current scroll position, for example).

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
Use <b>GetViewStateStream</b> when the view is being created to read in the saved view state and also when the view is being closed to save any changes to the view state. Typically, the view calls this method with <b>STGM_READ</b> when creating a view window and with <b>STGM_WRITE</b> when the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate">SaveViewState</a> method of its <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface is called.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Each Shell view should have its own view stream. Windows Explorer implements a most recently used (MRU) list of view streams that are stored on a per-user basis in the registry.

See also <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>