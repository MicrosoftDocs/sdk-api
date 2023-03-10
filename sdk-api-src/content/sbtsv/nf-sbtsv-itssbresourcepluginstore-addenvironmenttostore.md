---
UID: NF:sbtsv.ITsSbResourcePluginStore.AddEnvironmentToStore
title: ITsSbResourcePluginStore::AddEnvironmentToStore (sbtsv.h)
description: Adds an environment to the resource plug-in store.
helpviewer_keywords: ["AddEnvironmentToStore","AddEnvironmentToStore method [Remote Desktop Services]","AddEnvironmentToStore method [Remote Desktop Services]","ITsSbResourcePluginStore interface","AddEnvironmentToStore method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","ITsSbResourcePluginStore interface [Remote Desktop Services]","AddEnvironmentToStore method","ITsSbResourcePluginStore.AddEnvironmentToStore","ITsSbResourcePluginStore::AddEnvironmentToStore","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","AddEnvironmentToStore method","ITsSbResourcePluginStoreEx::AddEnvironmentToStore","sbtsv/ITsSbResourcePluginStore::AddEnvironmentToStore","sbtsv/ITsSbResourcePluginStoreEx::AddEnvironmentToStore","termserv.itssbresourcepluginstore_addenvironmenttostore"]
old-location: termserv\itssbresourcepluginstore_addenvironmenttostore.htm
tech.root: TermServ
ms.assetid: 5f1d995b-10de-4754-9160-fb93a9d8f263
ms.date: 12/05/2018
ms.keywords: AddEnvironmentToStore, AddEnvironmentToStore method [Remote Desktop Services], AddEnvironmentToStore method [Remote Desktop Services],ITsSbResourcePluginStore interface, AddEnvironmentToStore method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],AddEnvironmentToStore method, ITsSbResourcePluginStore.AddEnvironmentToStore, ITsSbResourcePluginStore::AddEnvironmentToStore, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],AddEnvironmentToStore method, ITsSbResourcePluginStoreEx::AddEnvironmentToStore, sbtsv/ITsSbResourcePluginStore::AddEnvironmentToStore, sbtsv/ITsSbResourcePluginStoreEx::AddEnvironmentToStore, termserv.itssbresourcepluginstore_addenvironmenttostore
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
 - ITsSbResourcePluginStore::AddEnvironmentToStore
 - sbtsv/ITsSbResourcePluginStore::AddEnvironmentToStore
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
 - ITsSbResourcePluginStore.AddEnvironmentToStore
 - ITsSbResourcePluginStoreEx.AddEnvironmentToStore
---

# ITsSbResourcePluginStore::AddEnvironmentToStore


## -description

Adds an environment to the resource plug-in store.

## -parameters

### -param pEnvironment [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a> environment object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Resource plug-ins can use this  method to add an environment to the resource plug-in store.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>