---
UID: NF:shobjidl_core.IFolderViewSettings.GetViewMode
title: IFolderViewSettings::GetViewMode
author: windows-sdk-content
description: Gets a folder's logical view mode.
old-location: shell\IFolderViewSettings_GetViewMode.htm
tech.root: shell
ms.assetid: 4b050a69-39df-41f8-8d54-8c576bad3c2d
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetViewMode, GetViewMode method [Windows Shell], GetViewMode method [Windows Shell],IFolderViewSettings interface, IFolderViewSettings interface [Windows Shell],GetViewMode method, IFolderViewSettings.GetViewMode, IFolderViewSettings::GetViewMode, _shell_IFolderViewSettings_GetViewMode, shell.IFolderViewSettings_GetViewMode, shobjidl_core/IFolderViewSettings::GetViewMode
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFolderViewSettings.GetViewMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderViewSettings::GetViewMode


## -description


Gets a folder's logical view mode.


## -parameters




### -param plvm [out]

Type: <b><a href="https://msdn.microsoft.com/4b30a335-ed80-4774-82d4-bc93c95ee80c">FOLDERLOGICALVIEWMODE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4b30a335-ed80-4774-82d4-bc93c95ee80c">FOLDERLOGICALVIEWMODE</a> value.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



