---
UID: NF:sbtsv.ITsSbResourcePluginStore.AddSessionToStore
title: ITsSbResourcePluginStore::AddSessionToStore (sbtsv.h)
description: Adds a new session to the resource plug-in store.
helpviewer_keywords: ["AddSessionToStore","AddSessionToStore method [Remote Desktop Services]","AddSessionToStore method [Remote Desktop Services]","ITsSbResourcePluginStore interface","AddSessionToStore method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","ITsSbResourcePluginStore interface [Remote Desktop Services]","AddSessionToStore method","ITsSbResourcePluginStore.AddSessionToStore","ITsSbResourcePluginStore::AddSessionToStore","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","AddSessionToStore method","ITsSbResourcePluginStoreEx::AddSessionToStore","sbtsv/ITsSbResourcePluginStore::AddSessionToStore","sbtsv/ITsSbResourcePluginStoreEx::AddSessionToStore","termserv.itssbresourcepluginstore_addsessiontostore"]
old-location: termserv\itssbresourcepluginstore_addsessiontostore.htm
tech.root: TermServ
ms.assetid: 354ca945-cefe-42f6-a255-9918b8ffc339
ms.date: 12/05/2018
ms.keywords: AddSessionToStore, AddSessionToStore method [Remote Desktop Services], AddSessionToStore method [Remote Desktop Services],ITsSbResourcePluginStore interface, AddSessionToStore method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],AddSessionToStore method, ITsSbResourcePluginStore.AddSessionToStore, ITsSbResourcePluginStore::AddSessionToStore, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],AddSessionToStore method, ITsSbResourcePluginStoreEx::AddSessionToStore, sbtsv/ITsSbResourcePluginStore::AddSessionToStore, sbtsv/ITsSbResourcePluginStoreEx::AddSessionToStore, termserv.itssbresourcepluginstore_addsessiontostore
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
 - ITsSbResourcePluginStore::AddSessionToStore
 - sbtsv/ITsSbResourcePluginStore::AddSessionToStore
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
 - ITsSbResourcePluginStore.AddSessionToStore
 - ITsSbResourcePluginStoreEx.AddSessionToStore
---

# ITsSbResourcePluginStore::AddSessionToStore


## -description

Adds a new session to the resource plug-in store. Call this method when a user has logged on to a new session.

## -parameters

### -param pSession [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession">ITsSbSession</a> session object. The target name, user name, domain name, and session ID are required fields.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession">ITsSbSession</a>