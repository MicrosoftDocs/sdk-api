---
UID: NF:shobjidl_core.IFolderView.SetCurrentViewMode
title: IFolderView::SetCurrentViewMode
author: windows-sdk-content
description: Sets the selected folder's view mode.
old-location: shell\IFolderView_SetCurrentViewMode.htm
tech.root: shell
ms.assetid: 7ca42567-7bb9-41e1-8f2a-5f6d0309c636
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: FVM_DETAILS, FVM_ICON, FVM_LIST, FVM_SMALLICON, FVM_THUMBNAIL, FVM_THUMBSTRIP, FVM_TILE, IFolderView interface [Windows Shell],SetCurrentViewMode method, IFolderView.SetCurrentViewMode, IFolderView::SetCurrentViewMode, SetCurrentViewMode, SetCurrentViewMode method [Windows Shell], SetCurrentViewMode method [Windows Shell],IFolderView interface, _shell_IFolderView_SetCurrentViewMode, shell.IFolderView_SetCurrentViewMode, shobjidl_core/IFolderView::SetCurrentViewMode
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
 - IFolderView.SetCurrentViewMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView::SetCurrentViewMode


## -description


Sets the selected folder's view mode.


## -parameters




### -param ViewMode [in]

Type: <b>UINT</b>

One of the following values from the <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a> enumeration.



#### FVM_ICON

Medium icons



#### FVM_SMALLICON

Small icons



#### FVM_LIST

List view without details. This view also uses small icons, but they cannot be rearranged as they can be when using <b>FVM_SMALLICON</b>.



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




<a href="https://msdn.microsoft.com/62d71bca-d2cb-4668-b0bf-2e53756f2cd9">CreateViewWindow</a>



<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/e8f69203-f0b4-4537-980c-8e5bbdb49aab">IFolderView::GetCurrentViewMode</a>
 

 

