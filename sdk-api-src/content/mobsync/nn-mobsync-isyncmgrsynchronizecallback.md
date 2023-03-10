---
UID: NN:mobsync.ISyncMgrSynchronizeCallback
title: ISyncMgrSynchronizeCallback (mobsync.h)
description: Exposes methods that manage the synchronization process.
helpviewer_keywords: ["ISyncMgrSynchronizeCallback","ISyncMgrSynchronizeCallback interface [Windows Shell]","ISyncMgrSynchronizeCallback interface [Windows Shell]","described","mobsync/ISyncMgrSynchronizeCallback","shell.syncmgr_isyncmgrsynchronizecallback","syncmgr.isyncmgrsynchronizecallback"]
old-location: shell\syncmgr_isyncmgrsynchronizecallback.htm
tech.root: shell
ms.assetid: 1c817a21-be91-43af-86c8-aa7909ae2fa2
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeCallback, ISyncMgrSynchronizeCallback interface [Windows Shell], ISyncMgrSynchronizeCallback interface [Windows Shell],described, mobsync/ISyncMgrSynchronizeCallback, shell.syncmgr_isyncmgrsynchronizecallback, syncmgr.isyncmgrsynchronizecallback
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
 - ISyncMgrSynchronizeCallback
 - mobsync/ISyncMgrSynchronizeCallback
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
 - ISyncMgrSynchronizeCallback
---

# ISyncMgrSynchronizeCallback interface


## -description

Exposes methods that manage the synchronization process.

## -inheritance

The <b>ISyncMgrSynchronizeCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSynchronizeCallback</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented by the synchronization manager to receive status, error, and progress information and display the user interface during the synchronization process.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications should call the methods of this interface as often as possible and must call it before starting each new ItemID to check whether the user has canceled an individual item.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>
