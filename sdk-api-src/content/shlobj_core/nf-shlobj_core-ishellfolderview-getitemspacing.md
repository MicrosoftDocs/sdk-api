---
UID: NF:shlobj_core.IShellFolderView.GetItemSpacing
title: IShellFolderView::GetItemSpacing (shlobj_core.h)
description: Gets the spacing for small and large view modes only.
helpviewer_keywords: ["GetItemSpacing","GetItemSpacing method [Windows Shell]","GetItemSpacing method [Windows Shell]","IShellFolderView interface","IShellFolderView interface [Windows Shell]","GetItemSpacing method","IShellFolderView.GetItemSpacing","IShellFolderView::GetItemSpacing","_shell_IShellFolderView_GetItemSpacing","shell.IShellFolderView_GetItemSpacing","shlobj_core/IShellFolderView::GetItemSpacing"]
old-location: shell\IShellFolderView_GetItemSpacing.htm
tech.root: shell
ms.assetid: 92450bc7-26e5-4061-90f7-eea0f0a4db09
ms.date: 12/05/2018
ms.keywords: GetItemSpacing, GetItemSpacing method [Windows Shell], GetItemSpacing method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetItemSpacing method, IShellFolderView.GetItemSpacing, IShellFolderView::GetItemSpacing, _shell_IShellFolderView_GetItemSpacing, shell.IShellFolderView_GetItemSpacing, shlobj_core/IShellFolderView::GetItemSpacing
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
 - IShellFolderView::GetItemSpacing
 - shlobj_core/IShellFolderView::GetItemSpacing
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
 - IShellFolderView.GetItemSpacing
---

# IShellFolderView::GetItemSpacing


## -description

<p class="CCE_Message">[This method has been deprecated. Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getspacing">IFolderView::GetSpacing</a> instead.]

Gets the spacing for small and large view modes only.

## -parameters

### -param pSpacing [out]

Type: <b><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing">ITEMSPACING</a>*</b>

A pointer to a structure that, when this method returns successfully, receives the information that describes the view mode spacing.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the current view mode is positionable; otherwise, <b>S_FALSE</b>.

## -remarks

This method sends an <a href="/windows/desktop/Controls/lvm-getitemspacing">LVM_GETITEMSPACING</a> message to get the view mode spacing.

This method retrieves mode spacing for only the large and small view modes.

In Windows Vista and later, this method stores the small view mode spacing in both pairs of values returned in the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing">ITEMSPACING</a> structure.