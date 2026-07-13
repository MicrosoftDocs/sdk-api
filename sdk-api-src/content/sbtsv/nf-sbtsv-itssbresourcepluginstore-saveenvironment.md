---
UID: NF:sbtsv.ITsSbResourcePluginStore.SaveEnvironment
title: ITsSbResourcePluginStore::SaveEnvironment (sbtsv.h)
description: Saves an environment.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","SaveEnvironment method","ITsSbResourcePluginStore.SaveEnvironment","ITsSbResourcePluginStore::SaveEnvironment","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","SaveEnvironment method","ITsSbResourcePluginStoreEx::SaveEnvironment","SaveEnvironment","SaveEnvironment method [Remote Desktop Services]","SaveEnvironment method [Remote Desktop Services]","ITsSbResourcePluginStore interface","SaveEnvironment method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","sbtsv/ITsSbResourcePluginStore::SaveEnvironment","sbtsv/ITsSbResourcePluginStoreEx::SaveEnvironment","termserv.itssbresourcepluginstore_saveenvironment"]
old-location: termserv\itssbresourcepluginstore_saveenvironment.htm
tech.root: TermServ
ms.assetid: 941d5040-e6e4-4f7e-be31-2b52eb16fa9f
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SaveEnvironment method, ITsSbResourcePluginStore.SaveEnvironment, ITsSbResourcePluginStore::SaveEnvironment, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],SaveEnvironment method, ITsSbResourcePluginStoreEx::SaveEnvironment, SaveEnvironment, SaveEnvironment method [Remote Desktop Services], SaveEnvironment method [Remote Desktop Services],ITsSbResourcePluginStore interface, SaveEnvironment method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::SaveEnvironment, sbtsv/ITsSbResourcePluginStoreEx::SaveEnvironment, termserv.itssbresourcepluginstore_saveenvironment
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
 - ITsSbResourcePluginStore::SaveEnvironment
 - sbtsv/ITsSbResourcePluginStore::SaveEnvironment
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
 - ITsSbResourcePluginStore.SaveEnvironment
 - ITsSbResourcePluginStoreEx.SaveEnvironment
---

# ITsSbResourcePluginStore::SaveEnvironment


## -description

Saves an environment.

## -parameters

### -param pEnvironment [in]

Pointer to the <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a> object to save.

### -param bForceWrite [in]

Set to <b>TRUE</b> to force writing the saved object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>