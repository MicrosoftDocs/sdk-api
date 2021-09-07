---
UID: NF:shobjidl_core.IFolderViewSettings.GetFolderFlags
title: IFolderViewSettings::GetFolderFlags (shobjidl_core.h)
description: Gets folder view options flags.
helpviewer_keywords: ["GetFolderFlags","GetFolderFlags method [Windows Shell]","GetFolderFlags method [Windows Shell]","IFolderViewSettings interface","IFolderViewSettings interface [Windows Shell]","GetFolderFlags method","IFolderViewSettings.GetFolderFlags","IFolderViewSettings::GetFolderFlags","_shell_IFolderViewSettings_GetFolderFlags","shell.IFolderViewSettings_GetFolderFlags","shobjidl_core/IFolderViewSettings::GetFolderFlags"]
old-location: shell\IFolderViewSettings_GetFolderFlags.htm
tech.root: shell
ms.assetid: a3b21d20-179c-4d6c-ac2e-9001d6358e52
ms.date: 12/05/2018
ms.keywords: GetFolderFlags, GetFolderFlags method [Windows Shell], GetFolderFlags method [Windows Shell],IFolderViewSettings interface, IFolderViewSettings interface [Windows Shell],GetFolderFlags method, IFolderViewSettings.GetFolderFlags, IFolderViewSettings::GetFolderFlags, _shell_IFolderViewSettings_GetFolderFlags, shell.IFolderViewSettings_GetFolderFlags, shobjidl_core/IFolderViewSettings::GetFolderFlags
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
 - IFolderViewSettings::GetFolderFlags
 - shobjidl_core/IFolderViewSettings::GetFolderFlags
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
 - IFolderViewSettings.GetFolderFlags
---

# IFolderViewSettings::GetFolderFlags


## -description

Gets folder view options flags.

## -parameters

### -param pfolderMask [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a>*</b>

A pointer to a mask for folder view options.

### -param pfolderFlags [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a>*</b>

A pointer to a flag for folder view options.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.