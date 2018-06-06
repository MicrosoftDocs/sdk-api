---
UID: NF:shobjidl_core.IFolderView2.GetViewModeAndIconSize
title: IFolderView2::GetViewModeAndIconSize
author: windows-sdk-content
description: Gets the current view mode and icon size applied to the view.
old-location: shell\IFolderView2_GetViewModeAndIconSize.htm
old-project: shell
ms.assetid: 4696d55e-aad7-41f2-b2c0-47d4b507c70c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetViewModeAndIconSize, GetViewModeAndIconSize method [Windows Shell], GetViewModeAndIconSize method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetViewModeAndIconSize method, IFolderView2.GetViewModeAndIconSize, IFolderView2::GetViewModeAndIconSize, _shell_IFolderView2_GetViewModeAndIconSize, shell.IFolderView2_GetViewModeAndIconSize, shobjidl_core/IFolderView2::GetViewModeAndIconSize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderView2.GetViewModeAndIconSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderView2::GetViewModeAndIconSize


## -description


Gets the current view mode and icon size applied to the view.


## -parameters




### -param puViewMode [out]

Type: <b><a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a>*</b>

A pointer to the current <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a>.


### -param piImageSize [out]

Type: <b>int*</b>

A pointer to the size of the icon in pixels.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



