---
UID: NN:syncmgr.ISyncMgrSyncItemInfo
title: ISyncMgrSyncItemInfo (syncmgr.h)
description: Exposes methods that provide property and state information for a single sync item.
helpviewer_keywords: ["ISyncMgrSyncItemInfo","ISyncMgrSyncItemInfo interface [Windows Shell]","ISyncMgrSyncItemInfo interface [Windows Shell]","described","_shell_ISyncMgrSyncItemInfo","shell.ISyncMgrSyncItemInfo","syncmgr/ISyncMgrSyncItemInfo"]
old-location: shell\ISyncMgrSyncItemInfo.htm
tech.root: shell
ms.assetid: b98d216e-f23f-45f3-b42d-e5aa2e540265
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncItemInfo, ISyncMgrSyncItemInfo interface [Windows Shell], ISyncMgrSyncItemInfo interface [Windows Shell],described, _shell_ISyncMgrSyncItemInfo, shell.ISyncMgrSyncItemInfo, syncmgr/ISyncMgrSyncItemInfo
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
 - ISyncMgrSyncItemInfo
 - syncmgr/ISyncMgrSyncItemInfo
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
 - ISyncMgrSyncItemInfo
---

# ISyncMgrSyncItemInfo interface


## -description

Exposes methods that provide property and state information for a single sync item.

## -inheritance

The <b>ISyncMgrSyncItemInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncItemInfo</b> also has these types of members:

## -remarks

By representing these properties as an interface, the set of properties can be changed later without recompiling the handler. The interface also provides type-safe access to the properties.

Items should always implement this interface, usually on the same object that implements <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitem">ISyncMgrSyncItem</a>.
