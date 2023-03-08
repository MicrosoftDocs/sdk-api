---
UID: NN:syncmgr.ISyncMgrHandler
title: ISyncMgrHandler (syncmgr.h)
description: Exposes methods that make up the primary interface implemented by a sync handler.
helpviewer_keywords: ["ISyncMgrHandler","ISyncMgrHandler interface [Windows Shell]","ISyncMgrHandler interface [Windows Shell]","described","_shell_ISyncMgrHandler","shell.ISyncMgrHandler","syncmgr/ISyncMgrHandler"]
old-location: shell\ISyncMgrHandler.htm
tech.root: shell
ms.assetid: 39579030-1cf5-4e82-a5e7-cb3415903d02
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandler, ISyncMgrHandler interface [Windows Shell], ISyncMgrHandler interface [Windows Shell],described, _shell_ISyncMgrHandler, shell.ISyncMgrHandler, syncmgr/ISyncMgrHandler
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
 - ISyncMgrHandler
 - syncmgr/ISyncMgrHandler
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
 - ISyncMgrHandler
---

# ISyncMgrHandler interface


## -description

Exposes methods that make up the primary interface implemented by a sync handler. Sync Center creates one instance of the handler through this interface to get properties, enumerate sync items, and modify state. Sync Center creates a separate instance of the handler on a separate thread to perform a synchronization or a UI operation.

## -inheritance

The <b>ISyncMgrHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrHandler</b> also has these types of members:

## -remarks

<b>ISyncMgrHandler</b> replaces <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>. Some of the earlier functionality has been streamlined, while some has been moved to other interfaces. See the individual method pages for specific information.
