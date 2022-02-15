---
UID: NF:shlobj_core.IShellFolderView.UpdateObject
title: IShellFolderView::UpdateObject (shlobj_core.h)
description: UpdateObject may be altered or unavailable.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","UpdateObject method","IShellFolderView.UpdateObject","IShellFolderView::UpdateObject","UpdateObject","UpdateObject method [Windows Shell]","UpdateObject method [Windows Shell]","IShellFolderView interface","_shell_IShellFolderView_UpdateObject","shell.IShellFolderView_UpdateObject","shlobj_core/IShellFolderView::UpdateObject"]
old-location: shell\IShellFolderView_UpdateObject.htm
tech.root: shell
ms.assetid: aacc326f-30e3-4794-b158-77ccf24f8d01
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],UpdateObject method, IShellFolderView.UpdateObject, IShellFolderView::UpdateObject, UpdateObject, UpdateObject method [Windows Shell], UpdateObject method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_UpdateObject, shell.IShellFolderView_UpdateObject, shlobj_core/IShellFolderView::UpdateObject
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
 - IShellFolderView::UpdateObject
 - shlobj_core/IShellFolderView::UpdateObject
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
 - IShellFolderView.UpdateObject
---

# IShellFolderView::UpdateObject


## -description

<p class="CCE_Message">[<b>UpdateObject</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Replaces an item in a view with another item.

## -parameters

### -param pidlOld [in]

Type: <b>PUITEMID_CHILD</b>

The original item.

### -param pidlNew [in]

Type: <b>PUITEMID_CHILD</b>

The new item.

### -param puItem [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the index of the item that was replaced. You can use this value to call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getobject">IShellFolderView::GetObject</a> on later to get back the PITEMID_CHILD that you just added.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you immediately call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getobject">IShellFolderView::GetObject</a> with the index returned by <i>puItem</i>, you will get a copy of the ITEMID_CHILD that you added.  However, the index position of an item may change over time, so code cannot trust that any specific index always returns the same ITEMID_CHILD.

Changes made through this method can be discarded in the view by the data source at any time.