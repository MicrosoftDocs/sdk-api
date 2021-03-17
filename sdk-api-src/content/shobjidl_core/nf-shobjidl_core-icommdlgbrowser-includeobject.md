---
UID: NF:shobjidl_core.ICommDlgBrowser.IncludeObject
title: ICommDlgBrowser::IncludeObject (shobjidl_core.h)
description: Allows the common dialog box to filter objects that the view displays.
helpviewer_keywords: ["ICommDlgBrowser interface [Windows Shell]","IncludeObject method","ICommDlgBrowser.IncludeObject","ICommDlgBrowser::IncludeObject","IncludeObject","IncludeObject method [Windows Shell]","IncludeObject method [Windows Shell]","ICommDlgBrowser interface","_win32_ICommDlgBrowser_IncludeObject","shell.ICommDlgBrowser_IncludeObject","shobjidl_core/ICommDlgBrowser::IncludeObject"]
old-location: shell\ICommDlgBrowser_IncludeObject.htm
tech.root: shell
ms.assetid: f483dda2-5384-42b5-97ca-c7c6793d19a7
ms.date: 12/05/2018
ms.keywords: ICommDlgBrowser interface [Windows Shell],IncludeObject method, ICommDlgBrowser.IncludeObject, ICommDlgBrowser::IncludeObject, IncludeObject, IncludeObject method [Windows Shell], IncludeObject method [Windows Shell],ICommDlgBrowser interface, _win32_ICommDlgBrowser_IncludeObject, shell.ICommDlgBrowser_IncludeObject, shobjidl_core/ICommDlgBrowser::IncludeObject
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
 - ICommDlgBrowser::IncludeObject
 - shobjidl_core/ICommDlgBrowser::IncludeObject
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
 - ICommDlgBrowser.IncludeObject
---

# ICommDlgBrowser::IncludeObject


## -description

Allows the common dialog box to filter objects that the view displays.

## -parameters

### -param ppshv

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the view's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.

### -param pidl

Type: <b>LPCITEMIDLIST</b>

A PIDL, relative to the folder, that identifies the object.

## -returns

Type: <b>HRESULT</b>

The browser should return S_OK to include the object in the view, or S_FALSE to hide it.

## -remarks

This method is called by the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a> implementation when hosted in file dialog boxes. The enumerator calls this method to let the common dialog box filter out objects that should not be displayed. Typically, the file dialog boxes will get the display text of the item, and filter by the extension.

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
Call this method before returning an object in the Shell folder's IDLIST enumerator.

When dealing with data sources that have many items, such as libraries and searches, the callback to this method results in poor performance. To avoid that situation, implement <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icommdlgbrowser2-getviewflags">GetViewFlags</a> and return CDB2GVF_NOINCLUDEITEM. Doing so enables the view to skip calling <b>ICommDlgBrowser::IncludeObject</b>, thereby improving performance.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd940358(v=vs.85)">Explorer Browser Search Sample</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a>