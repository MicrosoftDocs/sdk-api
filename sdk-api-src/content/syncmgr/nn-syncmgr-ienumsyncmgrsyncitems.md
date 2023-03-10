---
UID: NN:syncmgr.IEnumSyncMgrSyncItems
title: IEnumSyncMgrSyncItems (syncmgr.h)
description: Exposes methods that enumerate the sync item objects managed by the handler.
helpviewer_keywords: ["IEnumSyncMgrSyncItems","IEnumSyncMgrSyncItems interface [Windows Shell]","IEnumSyncMgrSyncItems interface [Windows Shell]","described","_shell_IEnumSyncMgrSyncItems","shell.IEnumSyncMgrSyncItems","syncmgr/IEnumSyncMgrSyncItems"]
old-location: shell\IEnumSyncMgrSyncItems.htm
tech.root: shell
ms.assetid: 0d1695e2-6936-4f53-9594-e0e2bc69afd4
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrSyncItems, IEnumSyncMgrSyncItems interface [Windows Shell], IEnumSyncMgrSyncItems interface [Windows Shell],described, _shell_IEnumSyncMgrSyncItems, shell.IEnumSyncMgrSyncItems, syncmgr/IEnumSyncMgrSyncItems
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumSyncMgrSyncItems
 - syncmgr/IEnumSyncMgrSyncItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - IEnumSyncMgrSyncItems
---

# IEnumSyncMgrSyncItems interface


## -description

Exposes methods that enumerate the sync item objects managed by the handler.

## -inheritance

The <b>IEnumSyncMgrSyncItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSyncMgrSyncItems</b> also has these types of members:

## -remarks

A handler returns a pointer to an <b>IEnumSyncMgrSyncItems</b> interface from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator">ISyncMgrSyncItemContainer::GetSyncItemEnumerator</a>.
