---
UID: NF:shlobj_core.IShellFolderView.SetItemPos
title: IShellFolderView::SetItemPos (shlobj_core.h)
description: Sets the position of the given item.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","SetItemPos method","IShellFolderView.SetItemPos","IShellFolderView::SetItemPos","SetItemPos","SetItemPos method [Windows Shell]","SetItemPos method [Windows Shell]","IShellFolderView interface","_shell_IShellFolderView_SetItemPos","shell.IShellFolderView_SetItemPos","shlobj_core/IShellFolderView::SetItemPos"]
old-location: shell\IShellFolderView_SetItemPos.htm
tech.root: shell
ms.assetid: d905260c-fa68-4b39-9c94-a74e1ac71b95
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],SetItemPos method, IShellFolderView.SetItemPos, IShellFolderView::SetItemPos, SetItemPos, SetItemPos method [Windows Shell], SetItemPos method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_SetItemPos, shell.IShellFolderView_SetItemPos, shlobj_core/IShellFolderView::SetItemPos
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
 - IShellFolderView::SetItemPos
 - shlobj_core/IShellFolderView::SetItemPos
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
 - IShellFolderView.SetItemPos
---

# IShellFolderView::SetItemPos


## -description

<p class="CCE_Message">[This method has been deprecated. Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-selectandpositionitems">IFolderView::SelectAndPositionItems</a> instead.]

Sets the position of the given item.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL that corresponds to the item for which the position is being set.

### -param ppt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a structure that contains the new coordinates of the item relative to the ListView contained in the view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.