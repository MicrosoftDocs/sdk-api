---
UID: NF:syncmgr.IEnumSyncMgrSyncItems.Next
title: IEnumSyncMgrSyncItems::Next
author: windows-sdk-content
description: Gets the next batch of sync items from the handler.
old-location: shell\IEnumSyncMgrSyncItems_Next.htm
tech.root: shell
ms.assetid: b886e3a8-a94b-45ed-893b-889bef70ae6a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEnumSyncMgrSyncItems interface [Windows Shell],Next method, IEnumSyncMgrSyncItems.Next, IEnumSyncMgrSyncItems::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumSyncMgrSyncItems interface, _shell_IEnumSyncMgrSyncItems_Next, shell.IEnumSyncMgrSyncItems_Next, syncmgr/IEnumSyncMgrSyncItems::Next
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
 - IEnumSyncMgrSyncItems.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- syncmgr.h
: 
- IEnumSyncMgrSyncItems.Next
: 
---

# IEnumSyncMgrSyncItems::Next


## -description


Gets the next batch of sync items from the handler.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

This value must be 1.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a>**</b>

The address of an <a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a> interface pointer.


### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to the number of items fetched.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



