---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



