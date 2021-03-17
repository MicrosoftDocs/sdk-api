---
UID: NF:shlobj_core.IShellFolderView.IsBkDropTarget
title: IShellFolderView::IsBkDropTarget (shlobj_core.h)
description: IsBkDropTarget may be altered or unavailable.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","IsBkDropTarget method","IShellFolderView.IsBkDropTarget","IShellFolderView::IsBkDropTarget","IsBkDropTarget","IsBkDropTarget method [Windows Shell]","IsBkDropTarget method [Windows Shell]","IShellFolderView interface","_shell_IShellFolderView_IsBkDropTarget","shell.IShellFolderView_IsBkDropTarget","shlobj_core/IShellFolderView::IsBkDropTarget"]
old-location: shell\IShellFolderView_IsBkDropTarget.htm
tech.root: shell
ms.assetid: 6de58057-2bcd-480e-8b4a-6e59aad168dc
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],IsBkDropTarget method, IShellFolderView.IsBkDropTarget, IShellFolderView::IsBkDropTarget, IsBkDropTarget, IsBkDropTarget method [Windows Shell], IsBkDropTarget method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_IsBkDropTarget, shell.IShellFolderView_IsBkDropTarget, shlobj_core/IShellFolderView::IsBkDropTarget
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
 - IShellFolderView::IsBkDropTarget
 - shlobj_core/IShellFolderView::IsBkDropTarget
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
 - IShellFolderView.IsBkDropTarget
---

# IShellFolderView::IsBkDropTarget


## -description

<p class="CCE_Message">[<b>IsBkDropTarget</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Checks if the target of a drag-and-drop operation is the background of the view.

## -parameters

### -param pDropTarget [in, optional]

Type: <b><a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>*</b>

A pointer to the target of the drag-and-drop operation.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the target of the drag-and-drop operation is to the background of the view, S_FALSE otherwise.