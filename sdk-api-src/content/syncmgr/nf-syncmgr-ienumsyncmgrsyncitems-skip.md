---
UID: NF:syncmgr.IEnumSyncMgrSyncItems.Skip
title: IEnumSyncMgrSyncItems::Skip method
author: windows-driver-content
description: Skips forward in the enumeration the specified number of items.
old-location: shell\IEnumSyncMgrSyncItems_Skip.htm
old-project: shell
ms.assetid: a07038de-84dc-4371-b72f-c835efd73ffc
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IEnumSyncMgrSyncItems, IEnumSyncMgrSyncItems interface [Windows Shell], Skip method, IEnumSyncMgrSyncItems::Skip, Skip method [Windows Shell], Skip method [Windows Shell], IEnumSyncMgrSyncItems interface, Skip,IEnumSyncMgrSyncItems.Skip, _shell_IEnumSyncMgrSyncItems_Skip, shell.IEnumSyncMgrSyncItems_Skip, syncmgr/IEnumSyncMgrSyncItems::Skip
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
-	IEnumSyncMgrSyncItems.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumSyncMgrSyncItems::Skip method


## -description


Skips forward in the enumeration the specified number of items.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of items to skip.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



