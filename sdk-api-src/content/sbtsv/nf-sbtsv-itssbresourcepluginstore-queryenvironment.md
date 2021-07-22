---
UID: NF:sbtsv.ITsSbResourcePluginStore.QueryEnvironment
title: ITsSbResourcePluginStore::QueryEnvironment (sbtsv.h)
description: Returns the specified environment object.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","QueryEnvironment method","ITsSbResourcePluginStore.QueryEnvironment","ITsSbResourcePluginStore::QueryEnvironment","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","QueryEnvironment method","ITsSbResourcePluginStoreEx::QueryEnvironment","QueryEnvironment","QueryEnvironment method [Remote Desktop Services]","QueryEnvironment method [Remote Desktop Services]","ITsSbResourcePluginStore interface","QueryEnvironment method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","sbtsv/ITsSbResourcePluginStore::QueryEnvironment","sbtsv/ITsSbResourcePluginStoreEx::QueryEnvironment","termserv.itssbresourcepluginstore_queryenvironment"]
old-location: termserv\itssbresourcepluginstore_queryenvironment.htm
tech.root: TermServ
ms.assetid: 1497c638-ba9d-467e-8fbb-8467a43666cc
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],QueryEnvironment method, ITsSbResourcePluginStore.QueryEnvironment, ITsSbResourcePluginStore::QueryEnvironment, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],QueryEnvironment method, ITsSbResourcePluginStoreEx::QueryEnvironment, QueryEnvironment, QueryEnvironment method [Remote Desktop Services], QueryEnvironment method [Remote Desktop Services],ITsSbResourcePluginStore interface, QueryEnvironment method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::QueryEnvironment, sbtsv/ITsSbResourcePluginStoreEx::QueryEnvironment, termserv.itssbresourcepluginstore_queryenvironment
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
 - ITsSbResourcePluginStore::QueryEnvironment
 - sbtsv/ITsSbResourcePluginStore::QueryEnvironment
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
 - ITsSbResourcePluginStore.QueryEnvironment
 - ITsSbResourcePluginStoreEx.QueryEnvironment
---

# ITsSbResourcePluginStore::QueryEnvironment


## -description

Returns the specified environment object.

## -parameters

### -param EnvironmentName [in]

The name of the environment.

### -param ppEnvironment [out]

A pointer to the retrieved <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a> environment object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>