---
UID: NF:shobjidl_core.IObjectWithFolderEnumMode.SetMode
title: IObjectWithFolderEnumMode::SetMode
author: windows-sdk-content
description: Sets the enumeration mode of the parsed item.
old-location: shell\IObjectWithFolderEnumMode_SetMode.htm
old-project: shell
ms.assetid: 7e7271ec-47a7-42bf-ab02-26cd587448bd
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IObjectWithFolderEnumMode interface [Windows Shell],SetMode method, IObjectWithFolderEnumMode.SetMode, IObjectWithFolderEnumMode::SetMode, SetMode, SetMode method [Windows Shell], SetMode method [Windows Shell],IObjectWithFolderEnumMode interface, _shell_IObjectWithFolderEnumMode_SetMode, shell.IObjectWithFolderEnumMode_SetMode, shobjidl_core/IObjectWithFolderEnumMode::SetMode
ms.prod: windows
ms.technology: windows-sdk
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
 - IObjectWithFolderEnumMode.SetMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IObjectWithFolderEnumMode::SetMode


## -description


Sets the enumeration mode of the parsed item.


## -parameters




### -param feMode [in]

Type: <b><a href="https://msdn.microsoft.com/ef360e40-63c9-49a0-bcfa-1f2e2ff11a3a">FOLDER_ENUM_MODE</a></b>

One of the <a href="https://msdn.microsoft.com/ef360e40-63c9-49a0-bcfa-1f2e2ff11a3a">FOLDER_ENUM_MODE</a> values that specify the enumeration mode.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



