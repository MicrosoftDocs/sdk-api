---
UID: NN:syncmgr.IEnumSyncMgrEvents
title: IEnumSyncMgrEvents (syncmgr.h)
description: Exposes sync event enumeration methods.
helpviewer_keywords: ["IEnumSyncMgrEvents","IEnumSyncMgrEvents interface [Windows Shell]","IEnumSyncMgrEvents interface [Windows Shell]","described","_shell_IEnumSyncMgrEvents","shell.IEnumSyncMgrEvents","syncmgr/IEnumSyncMgrEvents"]
old-location: shell\IEnumSyncMgrEvents.htm
tech.root: shell
ms.assetid: 74d0c373-e9b1-4d9c-bdb6-caa743938e32
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrEvents, IEnumSyncMgrEvents interface [Windows Shell], IEnumSyncMgrEvents interface [Windows Shell],described, _shell_IEnumSyncMgrEvents, shell.IEnumSyncMgrEvents, syncmgr/IEnumSyncMgrEvents
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
 - IEnumSyncMgrEvents
 - syncmgr/IEnumSyncMgrEvents
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
 - IEnumSyncMgrEvents
---

# IEnumSyncMgrEvents interface


## -description

Exposes sync event enumeration methods.

## -inheritance

The <b>IEnumSyncMgrEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSyncMgrEvents</b> also has these types of members:

## -remarks

An event store returns a pointer to an <b>IEnumSyncMgrEvents</b> interface from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgreventstore-geteventenumerator">ISyncMgrEventStore::GetEventEnumerator</a>.
