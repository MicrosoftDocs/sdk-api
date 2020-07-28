---
UID: NF:shobjidl_core.IFolderView.GetDefaultSpacing
title: IFolderView::GetDefaultSpacing (shobjidl_core.h)
description: Gets a pointer to a POINT structure containing the default width (x) and height (y) measurements of an item, including the surrounding white space.
helpviewer_keywords: ["GetDefaultSpacing","GetDefaultSpacing method [Windows Shell]","GetDefaultSpacing method [Windows Shell]","IFolderView interface","IFolderView interface [Windows Shell]","GetDefaultSpacing method","IFolderView.GetDefaultSpacing","IFolderView::GetDefaultSpacing","_shell_IFolderView_GetDefaultSpacing","shell.IFolderView_GetDefaultSpacing","shobjidl_core/IFolderView::GetDefaultSpacing"]
old-location: shell\IFolderView_GetDefaultSpacing.htm
tech.root: shell
ms.assetid: eb5f2dd6-1257-4cfc-a222-88e6c3b524ce
ms.date: 12/05/2018
ms.keywords: GetDefaultSpacing, GetDefaultSpacing method [Windows Shell], GetDefaultSpacing method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetDefaultSpacing method, IFolderView.GetDefaultSpacing, IFolderView::GetDefaultSpacing, _shell_IFolderView_GetDefaultSpacing, shell.IFolderView_GetDefaultSpacing, shobjidl_core/IFolderView::GetDefaultSpacing
f1_keywords:
- shobjidl_core/IFolderView.GetDefaultSpacing
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IFolderView.GetDefaultSpacing
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderView::GetDefaultSpacing


## -description


Gets a pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure containing the default width (x) and height (y) measurements of an item, including the surrounding white space.


## -parameters




### -param ppt [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a>*</b>

Pointer to an existing structure to be filled with the default sizing dimensions of the items in the folder's view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getspacing">IFolderView::GetSpacing</a>
 

 

