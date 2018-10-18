---
UID: NF:shobjidl_core.IFolderView.GetCurrentViewMode
title: IFolderView::GetCurrentViewMode
author: windows-sdk-content
description: Gets an address containing a value representing the folder's current view mode.
old-location: shell\IFolderView_GetCurrentViewMode.htm
tech.root: shell
ms.assetid: e8f69203-f0b4-4537-980c-8e5bbdb49aab
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: FVM_DETAILS, FVM_ICON, FVM_LIST, FVM_SMALLICON, FVM_THUMBNAIL, FVM_THUMBSTRIP, FVM_TILE, GetCurrentViewMode, GetCurrentViewMode method [Windows Shell], GetCurrentViewMode method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetCurrentViewMode method, IFolderView.GetCurrentViewMode, IFolderView::GetCurrentViewMode, _shell_IFolderView_GetCurrentViewMode, shell.IFolderView_GetCurrentViewMode, shobjidl_core/IFolderView::GetCurrentViewMode
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFolderView.GetCurrentViewMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView::GetCurrentViewMode


## -description


Gets an address containing a value representing the folder's current view mode.


## -parameters




### -param pViewMode [out]

Type: <b>UINT*</b>

A pointer to a memory location at which to store the folder's current view mode. The value at that address is one of the following <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a> values.





#### FVM_ICON

Medium icons



#### FVM_SMALLICON

Small icons



#### FVM_LIST

List view without details



#### FVM_DETAILS

Show details (size, type, last modification date)



#### FVM_THUMBNAIL

Thumbnail view



#### FVM_TILE

Large icons



#### FVM_THUMBSTRIP

Filmstrip view


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/69d18b4f-3a68-420c-a184-05c2f69a5ec6">GetCurrentInfo</a>



<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/7ca42567-7bb9-41e1-8f2a-5f6d0309c636">IFolderView::SetCurrentViewMode</a>
 

 

