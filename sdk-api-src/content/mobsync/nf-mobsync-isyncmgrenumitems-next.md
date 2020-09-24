---
UID: NF:mobsync.ISyncMgrEnumItems.Next
title: ISyncMgrEnumItems::Next (mobsync.h)
description: Enumerates the next celt elements in the enumerator's list, returning them in rgelt along with the actual number of enumerated elements in pceltFetched.
helpviewer_keywords: ["ISyncMgrEnumItems interface [Windows Shell]","Next method","ISyncMgrEnumItems.Next","ISyncMgrEnumItems::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","ISyncMgrEnumItems interface","mobsync/ISyncMgrEnumItems::Next","shell.syncmgr_isyncmgrenumitems_next","syncmgr.isyncmgrenumitems_next"]
old-location: shell\syncmgr_isyncmgrenumitems_next.htm
tech.root: shell
ms.assetid: bb4ab08a-aa12-46f0-8c7d-82742b0b1538
ms.date: 12/05/2018
ms.keywords: ISyncMgrEnumItems interface [Windows Shell],Next method, ISyncMgrEnumItems.Next, ISyncMgrEnumItems::Next, Next, Next method [Windows Shell], Next method [Windows Shell],ISyncMgrEnumItems interface, mobsync/ISyncMgrEnumItems::Next, shell.syncmgr_isyncmgrenumitems_next, syncmgr.isyncmgrenumitems_next
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mobsync.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrEnumItems::Next
 - mobsync/ISyncMgrEnumItems::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrEnumItems.Next
---

# ISyncMgrEnumItems::Next


## -description

Enumerates the next <i>celt</i> elements in the enumerator's list, returning them in <i>rgelt</i> along with the actual number of enumerated elements in <i>pceltFetched</i>.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of items in the array.

### -param rgelt [out]

Type: <b><a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgritem">SYNCMGRITEM</a>*</b>

The address of array containing items.

### -param pceltFetched [out]

Type: <b>ULONG*</b>

The address of variable containing actual number of items.

## -returns

Type: <b>HRESULT</b>

Return S_OK if the method succeeds.

## -remarks

E_NOTIMPL is not allowed as a return value. If an error value is returned, no entries in the <i>rgelt</i> array are valid on exit and require no release.