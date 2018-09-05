---
UID: NF:shobjidl_core.IFolderViewSettings.GetFolderFlags
title: IFolderViewSettings::GetFolderFlags
author: windows-sdk-content
description: Gets folder view options flags.
old-location: shell\IFolderViewSettings_GetFolderFlags.htm
old-project: shell
ms.assetid: a3b21d20-179c-4d6c-ac2e-9001d6358e52
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetFolderFlags, GetFolderFlags method [Windows Shell], GetFolderFlags method [Windows Shell],IFolderViewSettings interface, IFolderViewSettings interface [Windows Shell],GetFolderFlags method, IFolderViewSettings.GetFolderFlags, IFolderViewSettings::GetFolderFlags, _shell_IFolderViewSettings_GetFolderFlags, shell.IFolderViewSettings_GetFolderFlags, shobjidl_core/IFolderViewSettings::GetFolderFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
 - IFolderViewSettings.GetFolderFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderViewSettings::GetFolderFlags


## -description


Gets folder view options flags.


## -parameters




### -param pfolderMask [out]

Type: <b><a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a>*</b>

A pointer to a mask for folder view options.


### -param pfolderFlags [out]

Type: <b><a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a>*</b>

A pointer to a flag for folder view options.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



