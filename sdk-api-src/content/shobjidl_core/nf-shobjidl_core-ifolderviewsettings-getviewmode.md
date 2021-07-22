---
UID: NF:shobjidl_core.IFolderViewSettings.GetViewMode
title: IFolderViewSettings::GetViewMode (shobjidl_core.h)
description: Gets a folder's logical view mode.
helpviewer_keywords: ["GetViewMode","GetViewMode method [Windows Shell]","GetViewMode method [Windows Shell]","IFolderViewSettings interface","IFolderViewSettings interface [Windows Shell]","GetViewMode method","IFolderViewSettings.GetViewMode","IFolderViewSettings::GetViewMode","_shell_IFolderViewSettings_GetViewMode","shell.IFolderViewSettings_GetViewMode","shobjidl_core/IFolderViewSettings::GetViewMode"]
old-location: shell\IFolderViewSettings_GetViewMode.htm
tech.root: shell
ms.assetid: 4b050a69-39df-41f8-8d54-8c576bad3c2d
ms.date: 12/05/2018
ms.keywords: GetViewMode, GetViewMode method [Windows Shell], GetViewMode method [Windows Shell],IFolderViewSettings interface, IFolderViewSettings interface [Windows Shell],GetViewMode method, IFolderViewSettings.GetViewMode, IFolderViewSettings::GetViewMode, _shell_IFolderViewSettings_GetViewMode, shell.IFolderViewSettings_GetViewMode, shobjidl_core/IFolderViewSettings::GetViewMode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderViewSettings::GetViewMode
 - shobjidl_core/IFolderViewSettings::GetViewMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderViewSettings.GetViewMode
---

# IFolderViewSettings::GetViewMode


## -description

Gets a folder's logical view mode.

## -parameters

### -param plvm [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode">FOLDERLOGICALVIEWMODE</a>*</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode">FOLDERLOGICALVIEWMODE</a> value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.