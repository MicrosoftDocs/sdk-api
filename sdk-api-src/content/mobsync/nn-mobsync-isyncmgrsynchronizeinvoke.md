---
UID: NN:mobsync.ISyncMgrSynchronizeInvoke
title: ISyncMgrSynchronizeInvoke (mobsync.h)
description: Exposes methods that enable a registered application to invoke the synchronization manager to update items.
helpviewer_keywords: ["ISyncMgrSynchronizeInvoke","ISyncMgrSynchronizeInvoke interface [Windows Shell]","ISyncMgrSynchronizeInvoke interface [Windows Shell]","described","mobsync/ISyncMgrSynchronizeInvoke","shell.syncmgr_isyncmgrsynchronizeinvoke","syncmgr.isyncmgrsynchronizeinvoke"]
old-location: shell\syncmgr_isyncmgrsynchronizeinvoke.htm
tech.root: shell
ms.assetid: 993fd482-39e0-4966-ba71-eed7e4b54f72
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeInvoke, ISyncMgrSynchronizeInvoke interface [Windows Shell], ISyncMgrSynchronizeInvoke interface [Windows Shell],described, mobsync/ISyncMgrSynchronizeInvoke, shell.syncmgr_isyncmgrsynchronizeinvoke, syncmgr.isyncmgrsynchronizeinvoke
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
 - ISyncMgrSynchronizeInvoke
 - mobsync/ISyncMgrSynchronizeInvoke
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
 - ISyncMgrSynchronizeInvoke
---

# ISyncMgrSynchronizeInvoke interface


## -description

Exposes methods that enable a registered application to invoke the synchronization manager to update items.

## -inheritance

The <b>ISyncMgrSynchronizeInvoke</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSynchronizeInvoke</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented by the synchronization manager.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
A registered application calls the methods of this interface to update all items or to update specific items.
