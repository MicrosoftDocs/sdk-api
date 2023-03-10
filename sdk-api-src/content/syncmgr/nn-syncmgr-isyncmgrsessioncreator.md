---
UID: NN:syncmgr.ISyncMgrSessionCreator
title: ISyncMgrSessionCreator (syncmgr.h)
description: Exposes a single method through which a handler or external application can notify Sync Center that synchronization has begun, as well as report progress and events.
helpviewer_keywords: ["ISyncMgrSessionCreator","ISyncMgrSessionCreator interface [Windows Shell]","ISyncMgrSessionCreator interface [Windows Shell]","described","_shell_ISyncMgrSessionCreator","shell.ISyncMgrSessionCreator","syncmgr/ISyncMgrSessionCreator"]
old-location: shell\ISyncMgrSessionCreator.htm
tech.root: shell
ms.assetid: dc9662c5-42fa-45d2-aadd-93a5fb25d27c
ms.date: 12/05/2018
ms.keywords: ISyncMgrSessionCreator, ISyncMgrSessionCreator interface [Windows Shell], ISyncMgrSessionCreator interface [Windows Shell],described, _shell_ISyncMgrSessionCreator, shell.ISyncMgrSessionCreator, syncmgr/ISyncMgrSessionCreator
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
 - ISyncMgrSessionCreator
 - syncmgr/ISyncMgrSessionCreator
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
 - ISyncMgrSessionCreator
---

# ISyncMgrSessionCreator interface


## -description

Exposes a single method through which a handler or external application can notify Sync Center that synchronization has begun, as well as report progress and events.

## -inheritance

The <b>ISyncMgrSessionCreator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSessionCreator</b> also has these types of members:

## -remarks

This interface is passed to the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">ISyncMgrHandler::Synchronize</a>. The handler can choose to create a session in its <b>Synchronize</b> implementation. This allows the handler to report progress and events itself or to signal a background process to report progress and events itself.

                

Alternatively, the handler can choose to signal an external process to create a CLSID_SyncMgrClient object. If a handler is implemented to perform automatic synchronizations in an external process such as a service, it must be able to provide progress reports to Sync Center so that Sync Center can update the UI for the user. The handler also must be able to add events to Sync Center's <b>Sync Results</b> folder. An external process creates the CLSID_SyncMgrClient object by passing the CLSCTX_SERVER flag and the <b>ISyncMgrSessionCreator</b> IID to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. This allows that process to report progress and events as well as to ask Sync Center whether the user canceled the synchronization. Note, however, that <b>ISyncMgrSessionCreator</b> cannot be marshaled to an external process.
