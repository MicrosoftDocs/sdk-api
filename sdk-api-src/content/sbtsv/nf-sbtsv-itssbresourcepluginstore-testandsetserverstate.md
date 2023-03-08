---
UID: NF:sbtsv.ITsSbResourcePluginStore.TestAndSetServerState
title: ITsSbResourcePluginStore::TestAndSetServerState (sbtsv.h)
description: Conditionally sets a new state on a server.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","TestAndSetServerState method","ITsSbResourcePluginStore.TestAndSetServerState","ITsSbResourcePluginStore::TestAndSetServerState","TestAndSetServerState","TestAndSetServerState method [Remote Desktop Services]","TestAndSetServerState method [Remote Desktop Services]","ITsSbResourcePluginStore interface","sbtsv/ITsSbResourcePluginStore::TestAndSetServerState","termserv.itssbresourcepluginstore_testandsetserverstate"]
old-location: termserv\itssbresourcepluginstore_testandsetserverstate.htm
tech.root: TermServ
ms.assetid: 5b209587-090e-4338-95b3-542e50412587
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],TestAndSetServerState method, ITsSbResourcePluginStore.TestAndSetServerState, ITsSbResourcePluginStore::TestAndSetServerState, TestAndSetServerState, TestAndSetServerState method [Remote Desktop Services], TestAndSetServerState method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::TestAndSetServerState, termserv.itssbresourcepluginstore_testandsetserverstate
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbResourcePluginStore::TestAndSetServerState
 - sbtsv/ITsSbResourcePluginStore::TestAndSetServerState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.TestAndSetServerState
---

# ITsSbResourcePluginStore::TestAndSetServerState


## -description

Conditionally sets a new state on a server.

## -parameters

### -param PoolName [in]

Name of the pool.

### -param ServerFQDN [in]

Fully qualified domain name (FQDN) of the server.

### -param NewState [in]

The state to set.

### -param TestState [in]

If set to <b>TARGET_UNKNOWN</b> or the current state of the server, the  server will be set as specified in the <i>NewState</i> parameter.

### -param pInitState [out]

On return, points to the previous state of the server.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>