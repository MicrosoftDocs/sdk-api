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

# ISyncMgrConflictItems::GetItem


## -description


Gets a specified conflict data item.


## -parameters




### -param iIndex [in]

Type: <b>UINT</b>

The index of the conflict item to retrieve.


### -param pItemInfo [out]

Type: <b><a href="https://msdn.microsoft.com/3be4a8ec-eeab-4453-a2cb-18cadf39464a">CONFIRM_CONFLICT_ITEM</a>*</b>

When this method returns successfully, contains a pointer to a <a href="https://msdn.microsoft.com/3be4a8ec-eeab-4453-a2cb-18cadf39464a">CONFIRM_CONFLICT_ITEM</a> structure that contains information about the conflict.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



