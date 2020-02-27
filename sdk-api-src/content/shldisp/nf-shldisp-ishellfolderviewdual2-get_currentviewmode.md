---
UID: NF:shldisp.IShellFolderViewDual2.get_CurrentViewMode
title: IShellFolderViewDual2::get_CurrentViewMode (shldisp.h)
description: Gets the current view mode of the current folder.
old-location: shell\IShellFolderViewDual2_get_CurrentViewMode.htm
tech.root: shell
ms.assetid: aa4bcb25-98f9-49c3-be25-abc6a5ecdcca
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual2 interface [Windows Shell],get_CurrentViewMode method, IShellFolderViewDual2.get_CurrentViewMode, IShellFolderViewDual2::get_CurrentViewMode, _shell_IShellFolderViewDual2_get_CurrentViewMode, get_CurrentViewMode, get_CurrentViewMode method [Windows Shell], get_CurrentViewMode method [Windows Shell],IShellFolderViewDual2 interface, shell.IShellFolderViewDual2_get_CurrentViewMode, shldisp/IShellFolderViewDual2::get_CurrentViewMode
f1_keywords:
- shldisp/IShellFolderViewDual2.get_CurrentViewMode
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shldisp.h
api_name:
- IShellFolderViewDual2.get_CurrentViewMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellFolderViewDual2::get_CurrentViewMode


## -description


Gets the current view mode of the current folder.


## -parameters




### -param pViewMode [out]

Type: <b>uint*</b>

When this method returns, contains a pointer to an unsigned integer that represents the current view mode. For a list of possible values see <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual2-put_currentviewmode">IShellFolderViewDual2::put_CurrentViewMode</a>
 

 

