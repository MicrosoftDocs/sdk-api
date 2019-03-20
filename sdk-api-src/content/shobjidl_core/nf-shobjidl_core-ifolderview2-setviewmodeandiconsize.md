---
UID: NF:shobjidl_core.IFolderView2.SetViewModeAndIconSize
title: IFolderView2::SetViewModeAndIconSize (shobjidl_core.h)
author: windows-sdk-content
description: Sets and applies the view mode and image size.
old-location: shell\IFolderView2_SetViewModeAndIconSize.htm
tech.root: shell
ms.assetid: 52724e5d-074f-4715-9dca-50ed22d8519e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetViewModeAndIconSize method, IFolderView2.SetViewModeAndIconSize, IFolderView2::SetViewModeAndIconSize, SetViewModeAndIconSize, SetViewModeAndIconSize method [Windows Shell], SetViewModeAndIconSize method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetViewModeAndIconSize, shell.IFolderView2_SetViewModeAndIconSize, shobjidl_core/IFolderView2::SetViewModeAndIconSize
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderView2.SetViewModeAndIconSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView2::SetViewModeAndIconSize


## -description


Sets and applies the view mode and image size.


## -parameters




### -param uViewMode [in]

Type: <b><a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a></b>

The <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a> to be applied.


### -param iImageSize [in]

Type: <b>int</b>

The size of the image in pixels.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>iImageSize</i> is -1 then the current default icon size for the view mode is used.



