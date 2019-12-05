---
UID: NF:syncmgr.ISyncMgrConflict.GetItemsArray
title: ISyncMgrConflict::GetItemsArray (syncmgr.h)
description: Retrieves a conflict items array.
old-location: shell\ISyncMgrConflict_GetItemsArray.htm
tech.root: shell
ms.assetid: 6c836522-fb04-4176-a9b3-7602ae2d71a1
ms.date: 12/05/2018
ms.keywords: GetItemsArray, GetItemsArray method [Windows Shell], GetItemsArray method [Windows Shell],ISyncMgrConflict interface, ISyncMgrConflict interface [Windows Shell],GetItemsArray method, ISyncMgrConflict.GetItemsArray, ISyncMgrConflict::GetItemsArray, _shell_ISyncMgrConflict_GetItemsArray, shell.ISyncMgrConflict_GetItemsArray, syncmgr/ISyncMgrConflict::GetItemsArray
ms.topic: method
f1_keywords:
- syncmgr/ISyncMgrConflict.GetItemsArray
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Syncmgr.h
api_name:
- ISyncMgrConflict.GetItemsArray
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrConflict::GetItemsArray


## -description


Retrieves a conflict items array.


## -parameters




### -param ppArray [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictitems">ISyncMgrConflictItems</a>**</b>

The address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictitems">ISyncMgrConflictItems</a> array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



