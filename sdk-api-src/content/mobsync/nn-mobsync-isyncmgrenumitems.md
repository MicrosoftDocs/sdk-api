---
UID: NN:mobsync.ISyncMgrEnumItems
title: ISyncMgrEnumItems (mobsync.h)
description: Exposes methods that enumerate through an array of SYNCMGRITEM structures.
helpviewer_keywords: ["ISyncMgrEnumItems","ISyncMgrEnumItems interface [Windows Shell]","ISyncMgrEnumItems interface [Windows Shell]","described","mobsync/ISyncMgrEnumItems","shell.syncmgr_isyncmgrenumitems","syncmgr.isyncmgrenumitems"]
old-location: shell\syncmgr_isyncmgrenumitems.htm
tech.root: shell
ms.assetid: d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec
ms.date: 12/05/2018
ms.keywords: ISyncMgrEnumItems, ISyncMgrEnumItems interface [Windows Shell], ISyncMgrEnumItems interface [Windows Shell],described, mobsync/ISyncMgrEnumItems, shell.syncmgr_isyncmgrenumitems, syncmgr.isyncmgrenumitems
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
 - ISyncMgrEnumItems
 - mobsync/ISyncMgrEnumItems
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
 - ISyncMgrEnumItems
---

# ISyncMgrEnumItems interface


## -description

Exposes methods that enumerate through an array of <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgritem">SYNCMGRITEM</a> structures. Each of these structures provides information about an item that can be synchronized. <b>ISyncMgrEnumItems</b> has the same methods as all standard enumerator interfaces: Next, Skip, Reset, and Clone.

## -inheritance

The <b>ISyncMgrEnumItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrEnumItems</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
If the registered application works with the synchronization manager to synchronize items, it must implement an enumerator object with this interface to enumerate through the items.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
The synchronization manager obtains a pointer to this interface and calls each method during the synchronization process.

## -see-also

<a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgritem">SYNCMGRITEM</a>
