---
UID: NF:shobjidl_core.IObjectWithFolderEnumMode.GetMode
title: IObjectWithFolderEnumMode::GetMode
author: windows-sdk-content
description: Retrieves the enumeration mode of the parsed item.
old-location: shell\IObjectWithFolderEnumMode_GetMode.htm
tech.root: shell
ms.assetid: 5d331255-2295-4f7b-b2d6-1238edcc15bb
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetMode, GetMode method [Windows Shell], GetMode method [Windows Shell],IObjectWithFolderEnumMode interface, IObjectWithFolderEnumMode interface [Windows Shell],GetMode method, IObjectWithFolderEnumMode.GetMode, IObjectWithFolderEnumMode::GetMode, _shell_IObjectWithFolderEnumMode_GetMode, shell.IObjectWithFolderEnumMode_GetMode, shobjidl_core/IObjectWithFolderEnumMode::GetMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IObjectWithFolderEnumMode.GetMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectWithFolderEnumMode::GetMode


## -description


Retrieves the enumeration mode of the parsed item.


## -parameters




### -param pfeMode [out]

Type: <b><a href="https://msdn.microsoft.com/ef360e40-63c9-49a0-bcfa-1f2e2ff11a3a">FOLDER_ENUM_MODE</a>*</b>

Pointer to a value that, when this method returns successfully, receives one of the <a href="https://msdn.microsoft.com/ef360e40-63c9-49a0-bcfa-1f2e2ff11a3a">FOLDER_ENUM_MODE</a> values specifying the enumeration mode.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



