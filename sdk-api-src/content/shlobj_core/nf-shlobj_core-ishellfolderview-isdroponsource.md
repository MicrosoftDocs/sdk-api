---
UID: NF:shlobj_core.IShellFolderView.IsDropOnSource
title: IShellFolderView::IsDropOnSource (shlobj_core.h)
description: Checks whether the destination of the current drag-and-drop or cut-and-paste operation is the same as the source.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","IsDropOnSource method","IShellFolderView.IsDropOnSource","IShellFolderView::IsDropOnSource","IsDropOnSource","IsDropOnSource method [Windows Shell]","IsDropOnSource method [Windows Shell]","IShellFolderView interface","_shell_IShellFolderView_IsDropOnSource","shell.IShellFolderView_IsDropOnSource","shlobj_core/IShellFolderView::IsDropOnSource"]
old-location: shell\IShellFolderView_IsDropOnSource.htm
tech.root: shell
ms.assetid: 3661fe68-b351-48e0-a098-8ad919bdfbb2
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],IsDropOnSource method, IShellFolderView.IsDropOnSource, IShellFolderView::IsDropOnSource, IsDropOnSource, IsDropOnSource method [Windows Shell], IsDropOnSource method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_IsDropOnSource, shell.IShellFolderView_IsDropOnSource, shlobj_core/IShellFolderView::IsDropOnSource
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
 - IShellFolderView::IsDropOnSource
 - shlobj_core/IShellFolderView::IsDropOnSource
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
 - IShellFolderView.IsDropOnSource
---

# IShellFolderView::IsDropOnSource


## -description

<p class="CCE_Message">[This method has been deprecated. Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-ismoveinsamefolder">IFolderView2::IsMoveInSameFolder</a> instead.]

Checks whether the destination of the current drag-and-drop or cut-and-paste operation is the same as the source.

## -parameters

### -param pDropTarget [in, optional]

Type: <b><a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>*</b>

A pointer to a destination drop target object.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the destination is the same as the source.