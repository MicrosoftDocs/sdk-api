---
UID: NF:shobjidl_core.IColumnManager.GetColumnCount
title: IColumnManager::GetColumnCount
author: windows-sdk-content
description: Gets the column count for either the visible columns or the complete set of columns.
old-location: shell\IColumnManager_GetColumnCount.htm
old-project: shell
ms.assetid: ab01c803-860e-4a16-9ed1-4c978af5b150
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetColumnCount, GetColumnCount method [Windows Shell], GetColumnCount method [Windows Shell],IColumnManager interface, IColumnManager interface [Windows Shell],GetColumnCount method, IColumnManager.GetColumnCount, IColumnManager::GetColumnCount, shell.IColumnManager_GetColumnCount, shell_IColumnManager_GetColumnCount, shobjidl_core/IColumnManager::GetColumnCount
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IColumnManager.GetColumnCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IColumnManager::GetColumnCount


## -description


Gets the column count for either the visible columns or the complete set of columns.


## -parameters




### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/9706ae59-d172-4518-8090-375b1a0ff4fb">CM_ENUM_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/9706ae59-d172-4518-8090-375b1a0ff4fb">CM_ENUM_FLAGS</a> enumeration that specifies whether to show only visible columns or all columns regardless of visibility.


### -param puCount [out]

Type: <b>UINT*</b>

Contains a pointer to the column count.


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.



