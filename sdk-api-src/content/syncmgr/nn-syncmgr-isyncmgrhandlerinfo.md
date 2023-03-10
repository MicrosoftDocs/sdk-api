---
UID: NN:syncmgr.ISyncMgrHandlerInfo
title: ISyncMgrHandlerInfo (syncmgr.h)
description: Exposes methods that allow a handler to provide property and state information to Sync Center.
helpviewer_keywords: ["ISyncMgrHandlerInfo","ISyncMgrHandlerInfo interface [Windows Shell]","ISyncMgrHandlerInfo interface [Windows Shell]","described","_shell_ISyncMgrHandlerInfo","shell.ISyncMgrHandlerInfo","syncmgr/ISyncMgrHandlerInfo"]
old-location: shell\ISyncMgrHandlerInfo.htm
tech.root: shell
ms.assetid: 29cded59-d0f3-4678-9601-4931687b48e4
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandlerInfo, ISyncMgrHandlerInfo interface [Windows Shell], ISyncMgrHandlerInfo interface [Windows Shell],described, _shell_ISyncMgrHandlerInfo, shell.ISyncMgrHandlerInfo, syncmgr/ISyncMgrHandlerInfo
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
 - ISyncMgrHandlerInfo
 - syncmgr/ISyncMgrHandlerInfo
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
 - ISyncMgrHandlerInfo
---

# ISyncMgrHandlerInfo interface


## -description

Exposes methods that allow a handler to provide property and state information to Sync Center.

## -inheritance

The <b>ISyncMgrHandlerInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrHandlerInfo</b> also has these types of members:

## -remarks

Handlers should always implement this interface, generally on the same object that implements <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a>. By implementing <b>ISyncMgrHandlerInfo</b>, the set of properties can be changed without requiring the handler to be recompiled. It also provides type-safe access to the properties.
