---
UID: NF:shlobj_core.IShellFolderView.GetSelectedCount
title: IShellFolderView::GetSelectedCount
author: windows-sdk-content
description: Gets the number of items in the view that are selected.
old-location: shell\IShellFolderView_GetSelectedCount.htm
tech.root: shell
ms.assetid: 3d504eba-7fb8-44a0-9534-4e7995b9b5d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSelectedCount, GetSelectedCount method [Windows Shell], GetSelectedCount method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetSelectedCount method, IShellFolderView.GetSelectedCount, IShellFolderView::GetSelectedCount, _shell_IShellFolderView_GetSelectedCount, shell.IShellFolderView_GetSelectedCount, shlobj_core/IShellFolderView::GetSelectedCount
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.GetSelectedCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::GetSelectedCount


## -description


<p class="CCE_Message">[<b>GetSelectedCount</b> is no longer available for use as of Windows Vista. Instead, use <a href="https://msdn.microsoft.com/d8ff0c8f-9678-455b-b7ec-9b651df769bc">IFolderView2::GetSelection</a>.]

Gets the number of items in the view that are selected.


## -parameters




### -param puSelected [out]

Type: <b>UINT*</b>

A pointer to a value that, when this method returns successfully, receives the number of selected items in the view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



