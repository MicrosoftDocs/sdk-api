---
UID: NF:sbtsv.ITsSbResourcePluginStore.AddTargetToStore
title: ITsSbResourcePluginStore::AddTargetToStore (sbtsv.h)
description: Adds a target to the resource plug-in store.
helpviewer_keywords: ["AddTargetToStore","AddTargetToStore method [Remote Desktop Services]","AddTargetToStore method [Remote Desktop Services]","ITsSbResourcePluginStore interface","AddTargetToStore method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","ITsSbResourcePluginStore interface [Remote Desktop Services]","AddTargetToStore method","ITsSbResourcePluginStore.AddTargetToStore","ITsSbResourcePluginStore::AddTargetToStore","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","AddTargetToStore method","ITsSbResourcePluginStoreEx::AddTargetToStore","sbtsv/ITsSbResourcePluginStore::AddTargetToStore","sbtsv/ITsSbResourcePluginStoreEx::AddTargetToStore","termserv.itssbresourcepluginstore_addtargettostore"]
old-location: termserv\itssbresourcepluginstore_addtargettostore.htm
tech.root: TermServ
ms.assetid: 207761eb-b87a-44e5-9101-84d77f95fc23
ms.date: 12/05/2018
ms.keywords: AddTargetToStore, AddTargetToStore method [Remote Desktop Services], AddTargetToStore method [Remote Desktop Services],ITsSbResourcePluginStore interface, AddTargetToStore method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],AddTargetToStore method, ITsSbResourcePluginStore.AddTargetToStore, ITsSbResourcePluginStore::AddTargetToStore, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],AddTargetToStore method, ITsSbResourcePluginStoreEx::AddTargetToStore, sbtsv/ITsSbResourcePluginStore::AddTargetToStore, sbtsv/ITsSbResourcePluginStoreEx::AddTargetToStore, termserv.itssbresourcepluginstore_addtargettostore
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
 - ITsSbResourcePluginStore::AddTargetToStore
 - sbtsv/ITsSbResourcePluginStore::AddTargetToStore
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
 - ITsSbResourcePluginStore.AddTargetToStore
 - ITsSbResourcePluginStoreEx.AddTargetToStore
---

# ITsSbResourcePluginStore::AddTargetToStore


## -description

Adds a target to the resource plug-in store.

## -parameters

### -param pTarget [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> target object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>