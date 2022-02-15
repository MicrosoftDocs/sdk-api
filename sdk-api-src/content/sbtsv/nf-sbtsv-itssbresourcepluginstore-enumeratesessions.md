---
UID: NF:sbtsv.ITsSbResourcePluginStore.EnumerateSessions
title: ITsSbResourcePluginStore::EnumerateSessions (sbtsv.h)
description: Enumerates a specified set of sessions.
helpviewer_keywords: ["EnumerateSessions","EnumerateSessions method [Remote Desktop Services]","EnumerateSessions method [Remote Desktop Services]","ITsSbResourcePluginStore interface","EnumerateSessions method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","ITsSbResourcePluginStore interface [Remote Desktop Services]","EnumerateSessions method","ITsSbResourcePluginStore.EnumerateSessions","ITsSbResourcePluginStore::EnumerateSessions","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","EnumerateSessions method","ITsSbResourcePluginStoreEx::EnumerateSessions","sbtsv/ITsSbResourcePluginStore::EnumerateSessions","sbtsv/ITsSbResourcePluginStoreEx::EnumerateSessions","termserv.itssbresourcepluginstore_enumeratesessions"]
old-location: termserv\itssbresourcepluginstore_enumeratesessions.htm
tech.root: TermServ
ms.assetid: 217b5c28-b0f8-4a8f-8695-8c8e0895b508
ms.date: 12/05/2018
ms.keywords: EnumerateSessions, EnumerateSessions method [Remote Desktop Services], EnumerateSessions method [Remote Desktop Services],ITsSbResourcePluginStore interface, EnumerateSessions method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],EnumerateSessions method, ITsSbResourcePluginStore.EnumerateSessions, ITsSbResourcePluginStore::EnumerateSessions, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],EnumerateSessions method, ITsSbResourcePluginStoreEx::EnumerateSessions, sbtsv/ITsSbResourcePluginStore::EnumerateSessions, sbtsv/ITsSbResourcePluginStoreEx::EnumerateSessions, termserv.itssbresourcepluginstore_enumeratesessions
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
 - ITsSbResourcePluginStore::EnumerateSessions
 - sbtsv/ITsSbResourcePluginStore::EnumerateSessions
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
 - ITsSbResourcePluginStore.EnumerateSessions
 - ITsSbResourcePluginStoreEx.EnumerateSessions
---

# ITsSbResourcePluginStore::EnumerateSessions


## -description

Enumerates a specified set of sessions.

## -parameters

### -param targetName [in]

The name of the target.

### -param userName [in]

The name of the user account.

### -param userDomain [in]

The domain name of the user account.

### -param poolName [in]

The name of the pool.

### -param initialProgram [in]

The name of the published remote application.

### -param pSessionState [in]

A pointer to the  <a href="/windows/win32/api/sessdirpublictypes/ne-sessdirpublictypes-tssession_state">TSSESSION_STATE</a> value of the sessions to enumerate.

### -param pdwCount [in, out]

Returns a pointer to the number of sessions returned.

### -param ppVal [out]

Returns the list of sessions requested.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>