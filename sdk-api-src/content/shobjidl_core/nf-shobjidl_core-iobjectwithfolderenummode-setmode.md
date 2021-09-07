---
UID: NF:shobjidl_core.IObjectWithFolderEnumMode.SetMode
title: IObjectWithFolderEnumMode::SetMode (shobjidl_core.h)
description: Sets the enumeration mode of the parsed item.
helpviewer_keywords: ["IObjectWithFolderEnumMode interface [Windows Shell]","SetMode method","IObjectWithFolderEnumMode.SetMode","IObjectWithFolderEnumMode::SetMode","SetMode","SetMode method [Windows Shell]","SetMode method [Windows Shell]","IObjectWithFolderEnumMode interface","_shell_IObjectWithFolderEnumMode_SetMode","shell.IObjectWithFolderEnumMode_SetMode","shobjidl_core/IObjectWithFolderEnumMode::SetMode"]
old-location: shell\IObjectWithFolderEnumMode_SetMode.htm
tech.root: shell
ms.assetid: 7e7271ec-47a7-42bf-ab02-26cd587448bd
ms.date: 12/05/2018
ms.keywords: IObjectWithFolderEnumMode interface [Windows Shell],SetMode method, IObjectWithFolderEnumMode.SetMode, IObjectWithFolderEnumMode::SetMode, SetMode, SetMode method [Windows Shell], SetMode method [Windows Shell],IObjectWithFolderEnumMode interface, _shell_IObjectWithFolderEnumMode_SetMode, shell.IObjectWithFolderEnumMode_SetMode, shobjidl_core/IObjectWithFolderEnumMode::SetMode
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IObjectWithFolderEnumMode::SetMode
 - shobjidl_core/IObjectWithFolderEnumMode::SetMode
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
 - IObjectWithFolderEnumMode.SetMode
---

# IObjectWithFolderEnumMode::SetMode


## -description

Sets the enumeration mode of the parsed item.

## -parameters

### -param feMode [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode">FOLDER_ENUM_MODE</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode">FOLDER_ENUM_MODE</a> values that specify the enumeration mode.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.