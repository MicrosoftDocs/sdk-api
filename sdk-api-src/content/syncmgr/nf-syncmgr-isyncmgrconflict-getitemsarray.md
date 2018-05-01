---
UID: NF:syncmgr.ISyncMgrConflict.GetItemsArray
title: ISyncMgrConflict::GetItemsArray method
author: windows-driver-content
description: Retrieves a conflict items array.
old-location: shell\ISyncMgrConflict_GetItemsArray.htm
old-project: shell
ms.assetid: 6c836522-fb04-4176-a9b3-7602ae2d71a1
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetItemsArray method [Windows Shell], GetItemsArray method [Windows Shell], ISyncMgrConflict interface, GetItemsArray,ISyncMgrConflict.GetItemsArray, ISyncMgrConflict, ISyncMgrConflict interface [Windows Shell], GetItemsArray method, ISyncMgrConflict::GetItemsArray, _shell_ISyncMgrConflict_GetItemsArray, shell.ISyncMgrConflict_GetItemsArray, syncmgr/ISyncMgrConflict::GetItemsArray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrConflict.GetItemsArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflict::GetItemsArray method


## -description


Retrieves a conflict items array.


## -parameters




### -param ppArray [out]

Type: <b><a href="https://msdn.microsoft.com/1dea310d-137b-4180-99c9-e40cd4fa3a98">ISyncMgrConflictItems</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/1dea310d-137b-4180-99c9-e40cd4fa3a98">ISyncMgrConflictItems</a> array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



