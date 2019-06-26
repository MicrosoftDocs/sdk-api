---
UID: NF:syncmgr.ISyncMgrConflictItems.GetCount
title: ISyncMgrConflictItems::GetCount (syncmgr.h)
author: windows-sdk-content
description: Gets the conflict item count.
old-location: shell\ISyncMgrConflictItems_GetCount.htm
tech.root: shell
ms.assetid: 948223a2-289f-4372-bd5d-5a075b659804
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Shell], GetCount method [Windows Shell],ISyncMgrConflictItems interface, ISyncMgrConflictItems interface [Windows Shell],GetCount method, ISyncMgrConflictItems.GetCount, ISyncMgrConflictItems::GetCount, _shell_ISyncMgrConflictItems_GetCount, shell.ISyncMgrConflictItems_GetCount, syncmgr/ISyncMgrConflictItems::GetCount
ms.topic: method
f1_keywords: 
 - "syncmgr/ISyncMgrConflictItems.GetCount"
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
 - ISyncMgrConflictItems.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrConflictItems::GetCount


## -description


Gets the conflict item count.


## -parameters




### -param pCount [out]

Type: <b>UINT*</b>

A pointer to the item count.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



