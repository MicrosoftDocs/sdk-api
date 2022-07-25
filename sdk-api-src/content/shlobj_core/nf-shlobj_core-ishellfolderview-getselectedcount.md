---
UID: NF:shlobj_core.IShellFolderView.GetSelectedCount
title: IShellFolderView::GetSelectedCount (shlobj_core.h)
description: Gets the number of items in the view that are selected.
helpviewer_keywords: ["GetSelectedCount","GetSelectedCount method [Windows Shell]","GetSelectedCount method [Windows Shell]","IShellFolderView interface","IShellFolderView interface [Windows Shell]","GetSelectedCount method","IShellFolderView.GetSelectedCount","IShellFolderView::GetSelectedCount","_shell_IShellFolderView_GetSelectedCount","shell.IShellFolderView_GetSelectedCount","shlobj_core/IShellFolderView::GetSelectedCount"]
old-location: shell\IShellFolderView_GetSelectedCount.htm
tech.root: shell
ms.assetid: 3d504eba-7fb8-44a0-9534-4e7995b9b5d4
ms.date: 12/05/2018
ms.keywords: GetSelectedCount, GetSelectedCount method [Windows Shell], GetSelectedCount method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetSelectedCount method, IShellFolderView.GetSelectedCount, IShellFolderView::GetSelectedCount, _shell_IShellFolderView_GetSelectedCount, shell.IShellFolderView_GetSelectedCount, shlobj_core/IShellFolderView::GetSelectedCount
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolderView::GetSelectedCount
 - shlobj_core/IShellFolderView::GetSelectedCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.GetSelectedCount
---

# IShellFolderView::GetSelectedCount


## -description

<p class="CCE_Message">[<b>GetSelectedCount</b> is no longer available for use as of Windows Vista. Instead, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getselection">IFolderView2::GetSelection</a>.]

Gets the number of items in the view that are selected.

## -parameters

### -param puSelected [out]

Type: <b>UINT*</b>

A pointer to a value that, when this method returns successfully, receives the number of selected items in the view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.