---
UID: NF:shldisp.IShellFolderViewDual2.put_CurrentViewMode
title: IShellFolderViewDual2::put_CurrentViewMode (shldisp.h)
description: Sets the current view mode of the current folder.
helpviewer_keywords: ["IShellFolderViewDual2 interface [Windows Shell]","put_CurrentViewMode method","IShellFolderViewDual2.put_CurrentViewMode","IShellFolderViewDual2::put_CurrentViewMode","_shell_IShellFolderViewDual2_put_CurrentViewMode","put_CurrentViewMode","put_CurrentViewMode method [Windows Shell]","put_CurrentViewMode method [Windows Shell]","IShellFolderViewDual2 interface","shell.IShellFolderViewDual2_put_CurrentViewMode","shldisp/IShellFolderViewDual2::put_CurrentViewMode"]
old-location: shell\IShellFolderViewDual2_put_CurrentViewMode.htm
tech.root: shell
ms.assetid: 80f0e24e-8104-472e-b1d9-58d42f3925fe
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual2 interface [Windows Shell],put_CurrentViewMode method, IShellFolderViewDual2.put_CurrentViewMode, IShellFolderViewDual2::put_CurrentViewMode, _shell_IShellFolderViewDual2_put_CurrentViewMode, put_CurrentViewMode, put_CurrentViewMode method [Windows Shell], put_CurrentViewMode method [Windows Shell],IShellFolderViewDual2 interface, shell.IShellFolderViewDual2_put_CurrentViewMode, shldisp/IShellFolderViewDual2::put_CurrentViewMode
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
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
 - IShellFolderViewDual2::put_CurrentViewMode
 - shldisp/IShellFolderViewDual2::put_CurrentViewMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shldisp.h
api_name:
 - IShellFolderViewDual2.put_CurrentViewMode
---

# IShellFolderViewDual2::put_CurrentViewMode


## -description

Sets the current view mode of the current folder.

## -parameters

### -param ViewMode [in]

Type: <b>uint</b>

Sets the current view mode. For a list of possible values see <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual2-get_currentviewmode">IShellFolderViewDual2::get_CurrentViewMode</a>