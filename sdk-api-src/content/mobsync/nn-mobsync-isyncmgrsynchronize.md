---
UID: NN:mobsync.ISyncMgrSynchronize
title: ISyncMgrSynchronize (mobsync.h)
description: Exposes methods that enable the registered application or service to receive notifications from the synchronization manager.
helpviewer_keywords: ["ISyncMgrSynchronize","ISyncMgrSynchronize interface [Windows Shell]","ISyncMgrSynchronize interface [Windows Shell]","described","mobsync/ISyncMgrSynchronize","shell.syncmgr_isyncmgrsynchronize","syncmgr.isyncmgrsynchronize"]
old-location: shell\syncmgr_isyncmgrsynchronize.htm
tech.root: shell
ms.assetid: bb821672-10b1-4fe6-a752-6cd1ccd1e49e
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize, ISyncMgrSynchronize interface [Windows Shell], ISyncMgrSynchronize interface [Windows Shell],described, mobsync/ISyncMgrSynchronize, shell.syncmgr_isyncmgrsynchronize, syncmgr.isyncmgrsynchronize
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
 - ISyncMgrSynchronize
 - mobsync/ISyncMgrSynchronize
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
 - ISyncMgrSynchronize
---

# ISyncMgrSynchronize interface


## -description

Exposes methods that enable the registered application or service to receive notifications from the synchronization manager.

## -inheritance

The <b>ISyncMgrSynchronize</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSynchronize</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface should be implemented on the registered application's handler to receive notifications from the synchronization manager and to participate in the synchronization process.

<b>ISyncMgrSynchronize</b> has been replaced in Windows Vista by <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
The synchronization manager calls the methods of this interface to send notifications to the registered application or service during synchronization.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a>



<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>



<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizeinvoke">ISyncMgrSynchronizeInvoke</a>
