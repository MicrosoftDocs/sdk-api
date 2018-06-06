---
UID: NF:shobjidl_core.IFolderView.GetDefaultSpacing
title: IFolderView::GetDefaultSpacing
author: windows-sdk-content
description: Gets a pointer to a POINT structure containing the default width (x) and height (y) measurements of an item, including the surrounding white space.
old-location: shell\IFolderView_GetDefaultSpacing.htm
old-project: shell
ms.assetid: eb5f2dd6-1257-4cfc-a222-88e6c3b524ce
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDefaultSpacing, GetDefaultSpacing method [Windows Shell], GetDefaultSpacing method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetDefaultSpacing method, IFolderView.GetDefaultSpacing, IFolderView::GetDefaultSpacing, _shell_IFolderView_GetDefaultSpacing, shell.IFolderView_GetDefaultSpacing, shobjidl_core/IFolderView::GetDefaultSpacing
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderView.GetDefaultSpacing
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderView::GetDefaultSpacing


## -description


Gets a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure containing the default width (x) and height (y) measurements of an item, including the surrounding white space.


## -parameters




### -param ppt [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

Pointer to an existing structure to be filled with the default sizing dimensions of the items in the folder's view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/6ea81c40-773f-4f53-97c1-99619e46be48">IFolderView::GetSpacing</a>
 

 

