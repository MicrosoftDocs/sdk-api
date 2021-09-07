---
UID: NN:mobsync.ISyncMgrRegister
title: ISyncMgrRegister (mobsync.h)
description: Exposes methods so that an application can register with the synchronization manager. This can be achieved either through the ISyncMgrRegister interface or by registering directly in the registry.
helpviewer_keywords: ["ISyncMgrRegister","ISyncMgrRegister interface [Windows Shell]","ISyncMgrRegister interface [Windows Shell]","described","mobsync/ISyncMgrRegister","shell.syncmgr_isyncmgrregister","syncmgr.isyncmgrregister"]
old-location: shell\syncmgr_isyncmgrregister.htm
tech.root: shell
ms.assetid: 1feed230-5a50-4ff5-a8a9-e0ce15ba8f1c
ms.date: 12/05/2018
ms.keywords: ISyncMgrRegister, ISyncMgrRegister interface [Windows Shell], ISyncMgrRegister interface [Windows Shell],described, mobsync/ISyncMgrRegister, shell.syncmgr_isyncmgrregister, syncmgr.isyncmgrregister
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
 - ISyncMgrRegister
 - mobsync/ISyncMgrRegister
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
 - ISyncMgrRegister
---

# ISyncMgrRegister interface


## -description

Exposes methods so that an application can register with the synchronization manager. This can be achieved either through the 
<b>ISyncMgrRegister</b> interface or by registering directly in the registry.

## -inheritance

The <b>ISyncMgrRegister</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrRegister</b> also has these types of members:

## -remarks

The handler must be a standard OLE server. It must register the standard OLE keys for an InProc OLE server in addition to the SyncMgr key.
