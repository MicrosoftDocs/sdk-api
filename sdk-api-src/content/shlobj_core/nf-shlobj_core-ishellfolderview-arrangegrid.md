---
UID: NF:shlobj_core.IShellFolderView.ArrangeGrid
title: IShellFolderView::ArrangeGrid (shlobj_core.h)
description: Arranges moved icons so that they align to an invisible grid.
helpviewer_keywords: ["ArrangeGrid","ArrangeGrid method [Windows Shell]","ArrangeGrid method [Windows Shell]","IShellFolderView interface","IShellFolderView interface [Windows Shell]","ArrangeGrid method","IShellFolderView.ArrangeGrid","IShellFolderView::ArrangeGrid","_shell_IShellFolderView_ArrangeGrid","shell.IShellFolderView_ArrangeGrid","shlobj_core/IShellFolderView::ArrangeGrid"]
old-location: shell\IShellFolderView_ArrangeGrid.htm
tech.root: shell
ms.assetid: 3cb77a02-82da-42d3-97a3-ff47a9ce1831
ms.date: 12/05/2018
ms.keywords: ArrangeGrid, ArrangeGrid method [Windows Shell], ArrangeGrid method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],ArrangeGrid method, IShellFolderView.ArrangeGrid, IShellFolderView::ArrangeGrid, _shell_IShellFolderView_ArrangeGrid, shell.IShellFolderView_ArrangeGrid, shlobj_core/IShellFolderView::ArrangeGrid
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
 - IShellFolderView::ArrangeGrid
 - shlobj_core/IShellFolderView::ArrangeGrid
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
 - IShellFolderView.ArrangeGrid
---

# IShellFolderView::ArrangeGrid


## -description

<p class="CCE_Message">[<b>ArrangeGrid</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Arranges moved icons so that they align to an invisible grid.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method has the same effect as selecting <b>View | Arrange Icons By | Align to Grid</b> in Windows Explorer on Windows XP, and also the same as right-clicking the desktop and selecting <b>Arrange Icons By | Align to Grid</b> on Windows XP or Windows Vista.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderview">IShellFolderView</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-autoarrange">IShellFolderView::AutoArrange</a>
