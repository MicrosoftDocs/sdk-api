---
UID: NF:mobsync.ISyncMgrEnumItems.Reset
title: ISyncMgrEnumItems::Reset (mobsync.h)
description: Instructs the enumerator to position itself at the beginning of the list of elements.
helpviewer_keywords: ["ISyncMgrEnumItems interface [Windows Shell]","Reset method","ISyncMgrEnumItems.Reset","ISyncMgrEnumItems::Reset","Reset","Reset method [Windows Shell]","Reset method [Windows Shell]","ISyncMgrEnumItems interface","mobsync/ISyncMgrEnumItems::Reset","shell.syncmgr_isyncmgrenumitems_reset","syncmgr.isyncmgrenumitems_reset"]
old-location: shell\syncmgr_isyncmgrenumitems_reset.htm
tech.root: shell
ms.assetid: 91265648-1294-423d-8e09-6d14eb0b6d9e
ms.date: 12/05/2018
ms.keywords: ISyncMgrEnumItems interface [Windows Shell],Reset method, ISyncMgrEnumItems.Reset, ISyncMgrEnumItems::Reset, Reset, Reset method [Windows Shell], Reset method [Windows Shell],ISyncMgrEnumItems interface, mobsync/ISyncMgrEnumItems::Reset, shell.syncmgr_isyncmgrenumitems_reset, syncmgr.isyncmgrenumitems_reset
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
 - ISyncMgrEnumItems::Reset
 - mobsync/ISyncMgrEnumItems::Reset
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
 - ISyncMgrEnumItems.Reset
---

# ISyncMgrEnumItems::Reset


## -description

Instructs the enumerator to position itself at the beginning of the list of elements.



## -returns

Type: <b>HRESULT</b>

Return S_OK if the method succeeds.

## -remarks

There is no guarantee that the same set of elements are enumerated on each pass through the list, nor are the elements necessarily enumerated in the same order. The exact behavior depends on the collection being enumerated. The operation is too memory-intensive for some collections, such as files in a directory, to maintain a specific state.

