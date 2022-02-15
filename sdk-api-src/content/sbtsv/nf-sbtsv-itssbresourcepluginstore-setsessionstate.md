---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetSessionState
title: ITsSbResourcePluginStore::SetSessionState (sbtsv.h)
description: Sets the session state.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","SetSessionState method","ITsSbResourcePluginStore.SetSessionState","ITsSbResourcePluginStore::SetSessionState","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","SetSessionState method","ITsSbResourcePluginStoreEx::SetSessionState","SetSessionState","SetSessionState method [Remote Desktop Services]","SetSessionState method [Remote Desktop Services]","ITsSbResourcePluginStore interface","SetSessionState method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","sbtsv/ITsSbResourcePluginStore::SetSessionState","sbtsv/ITsSbResourcePluginStoreEx::SetSessionState","termserv.itssbresourcepluginstore_setsessionstate"]
old-location: termserv\itssbresourcepluginstore_setsessionstate.htm
tech.root: TermServ
ms.assetid: e6cb83d4-9d85-43d0-812d-ad6e2bdcb067
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetSessionState method, ITsSbResourcePluginStore.SetSessionState, ITsSbResourcePluginStore::SetSessionState, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],SetSessionState method, ITsSbResourcePluginStoreEx::SetSessionState, SetSessionState, SetSessionState method [Remote Desktop Services], SetSessionState method [Remote Desktop Services],ITsSbResourcePluginStore interface, SetSessionState method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::SetSessionState, sbtsv/ITsSbResourcePluginStoreEx::SetSessionState, termserv.itssbresourcepluginstore_setsessionstate
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - ITsSbResourcePluginStore::SetSessionState
 - sbtsv/ITsSbResourcePluginStore::SetSessionState
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
 - ITsSbResourcePluginStore.SetSessionState
 - ITsSbResourcePluginStoreEx.SetSessionState
---

# ITsSbResourcePluginStore::SetSessionState


## -description

Sets the session state.

## -parameters

### -param sbSession [in]

A pointer to the session to modify.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>