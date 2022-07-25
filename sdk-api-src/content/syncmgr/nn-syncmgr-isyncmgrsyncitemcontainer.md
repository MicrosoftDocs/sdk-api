---
UID: NN:syncmgr.ISyncMgrSyncItemContainer
title: ISyncMgrSyncItemContainer (syncmgr.h)
description: Exposes methods that provide information to handlers about the items they contain.
helpviewer_keywords: ["ISyncMgrSyncItemContainer","ISyncMgrSyncItemContainer interface [Windows Shell]","ISyncMgrSyncItemContainer interface [Windows Shell]","described","_shell_ISyncMgrSyncItemContainer","shell.ISyncMgrSyncItemContainer","syncmgr/ISyncMgrSyncItemContainer"]
old-location: shell\ISyncMgrSyncItemContainer.htm
tech.root: shell
ms.assetid: c07487a5-aa12-411d-93bd-3774262e55c6
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncItemContainer, ISyncMgrSyncItemContainer interface [Windows Shell], ISyncMgrSyncItemContainer interface [Windows Shell],described, _shell_ISyncMgrSyncItemContainer, shell.ISyncMgrSyncItemContainer, syncmgr/ISyncMgrSyncItemContainer
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
 - ISyncMgrSyncItemContainer
 - syncmgr/ISyncMgrSyncItemContainer
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
 - ISyncMgrSyncItemContainer
---

# ISyncMgrSyncItemContainer interface


## -description

Exposes methods that provide information to handlers about the items they contain.

## -inheritance

The <b>ISyncMgrSyncItemContainer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncItemContainer</b> also has these types of members:

## -remarks

Sync Center calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a> interface to obtain a pointer to the <b>ISyncMgrSyncItemContainer</b> interface.
