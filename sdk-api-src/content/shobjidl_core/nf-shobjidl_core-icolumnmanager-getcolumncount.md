---
UID: NF:shobjidl_core.IColumnManager.GetColumnCount
title: IColumnManager::GetColumnCount (shobjidl_core.h)
description: Gets the column count for either the visible columns or the complete set of columns.
helpviewer_keywords: ["GetColumnCount","GetColumnCount method [Windows Shell]","GetColumnCount method [Windows Shell]","IColumnManager interface","IColumnManager interface [Windows Shell]","GetColumnCount method","IColumnManager.GetColumnCount","IColumnManager::GetColumnCount","shell.IColumnManager_GetColumnCount","shell_IColumnManager_GetColumnCount","shobjidl_core/IColumnManager::GetColumnCount"]
old-location: shell\IColumnManager_GetColumnCount.htm
tech.root: shell
ms.assetid: ab01c803-860e-4a16-9ed1-4c978af5b150
ms.date: 12/05/2018
ms.keywords: GetColumnCount, GetColumnCount method [Windows Shell], GetColumnCount method [Windows Shell],IColumnManager interface, IColumnManager interface [Windows Shell],GetColumnCount method, IColumnManager.GetColumnCount, IColumnManager::GetColumnCount, shell.IColumnManager_GetColumnCount, shell_IColumnManager_GetColumnCount, shobjidl_core/IColumnManager::GetColumnCount
f1_keywords:
- shobjidl_core/IColumnManager.GetColumnCount
dev_langs:
- c++
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IColumnManager.GetColumnCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IColumnManager::GetColumnCount


## -description


Gets the column count for either the visible columns or the complete set of columns.


## -parameters




### -param dwFlags [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags">CM_ENUM_FLAGS</a></b>

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags">CM_ENUM_FLAGS</a> enumeration that specifies whether to show only visible columns or all columns regardless of visibility.


### -param puCount [out]

Type: <b>UINT*</b>

Contains a pointer to the column count.


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.



