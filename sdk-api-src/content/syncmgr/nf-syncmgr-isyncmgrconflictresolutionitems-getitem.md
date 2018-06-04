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

# ISyncMgrConflictResolutionItems::GetItem


## -description


Gets result information for a specified item, when successful.


## -parameters




### -param iIndex [in]

Type: <b>UINT</b>

The index of the item.


### -param pItemInfo [out]

Type: <b><a href="https://msdn.microsoft.com/572bb9b7-a33d-4323-9363-abb43d9411e6">CONFIRM_CONFLICT_RESULT_INFO</a>*</b>

On success, contains a pointer to a <a href="https://msdn.microsoft.com/572bb9b7-a33d-4323-9363-abb43d9411e6">CONFIRM_CONFLICT_RESULT_INFO</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



