---
UID: NN:syncmgr.ISyncMgrResolutionHandler
title: ISyncMgrResolutionHandler (syncmgr.h)
description: Exposes methods that manage synchronizing conflicts. Implement this interface to construct a sync conflict handler. The conflict resolution user interface (UI) will call this interface to resolve the conflict presented to the user.
helpviewer_keywords: ["ISyncMgrResolutionHandler","ISyncMgrResolutionHandler interface [Windows Shell]","ISyncMgrResolutionHandler interface [Windows Shell]","described","_shell_ISyncMgrResolutionHandler","shell.ISyncMgrResolutionHandler","syncmgr/ISyncMgrResolutionHandler"]
old-location: shell\ISyncMgrResolutionHandler.htm
tech.root: shell
ms.assetid: 5b77217d-5c63-41be-b4df-338714a90fb9
ms.date: 12/05/2018
ms.keywords: ISyncMgrResolutionHandler, ISyncMgrResolutionHandler interface [Windows Shell], ISyncMgrResolutionHandler interface [Windows Shell],described, _shell_ISyncMgrResolutionHandler, shell.ISyncMgrResolutionHandler, syncmgr/ISyncMgrResolutionHandler
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
 - ISyncMgrResolutionHandler
 - syncmgr/ISyncMgrResolutionHandler
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
 - ISyncMgrResolutionHandler
---

# ISyncMgrResolutionHandler interface


## -description

Exposes methods that manage synchronizing conflicts. Implement this interface to construct a sync conflict handler. The conflict resolution user interface (UI) will call this interface to resolve the conflict presented to the user.

## -inheritance

The <b>ISyncMgrResolutionHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrResolutionHandler</b> also has these types of members:

