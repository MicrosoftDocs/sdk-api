---
UID: NF:syncmgr.IEnumSyncMgrConflict.Next
title: IEnumSyncMgrConflict::Next
author: windows-sdk-content
description: Gets the next batch of conflicts from the conflicts store.
old-location: shell\IEnumSyncMgrConflict_Next.htm
old-project: shell
ms.assetid: 486fba93-cdd1-49fd-96a8-cf56d1775a7c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IEnumSyncMgrConflict interface [Windows Shell],Next method, IEnumSyncMgrConflict.Next, IEnumSyncMgrConflict::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumSyncMgrConflict interface, _shell_IEnumSyncMgrConflict_Next, shell.IEnumSyncMgrConflict_Next, syncmgr/IEnumSyncMgrConflict::Next
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - IEnumSyncMgrConflict.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumSyncMgrConflict::Next


## -description


Gets the next batch of conflicts from the conflicts store.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The value must be 1.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/a5806a83-b470-4617-961d-b768160afc48">ISyncMgrConflict</a>**</b>

The address of an <a href="https://msdn.microsoft.com/a5806a83-b470-4617-961d-b768160afc48">ISyncMgrConflict</a> interface pointer.


### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to the number of conflicts fetched.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



