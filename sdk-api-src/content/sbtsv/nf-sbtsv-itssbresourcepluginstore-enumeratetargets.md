---
UID: NF:sbtsv.ITsSbResourcePluginStore.EnumerateTargets
title: ITsSbResourcePluginStore::EnumerateTargets (sbtsv.h)
description: Returns an array that contains the specified targets that are present in the resource plug-in store.
helpviewer_keywords: ["EnumerateTargets","EnumerateTargets method [Remote Desktop Services]","EnumerateTargets method [Remote Desktop Services]","ITsSbResourcePluginStore interface","EnumerateTargets method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","ITsSbResourcePluginStore interface [Remote Desktop Services]","EnumerateTargets method","ITsSbResourcePluginStore.EnumerateTargets","ITsSbResourcePluginStore::EnumerateTargets","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","EnumerateTargets method","ITsSbResourcePluginStoreEx::EnumerateTargets","sbtsv/ITsSbResourcePluginStore::EnumerateTargets","sbtsv/ITsSbResourcePluginStoreEx::EnumerateTargets","termserv.itssbresourcepluginstore_enumeratetargets"]
old-location: termserv\itssbresourcepluginstore_enumeratetargets.htm
tech.root: TermServ
ms.assetid: bb05847a-e7fb-481b-ad84-9f6dc15f9be0
ms.date: 12/05/2018
ms.keywords: EnumerateTargets, EnumerateTargets method [Remote Desktop Services], EnumerateTargets method [Remote Desktop Services],ITsSbResourcePluginStore interface, EnumerateTargets method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],EnumerateTargets method, ITsSbResourcePluginStore.EnumerateTargets, ITsSbResourcePluginStore::EnumerateTargets, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],EnumerateTargets method, ITsSbResourcePluginStoreEx::EnumerateTargets, sbtsv/ITsSbResourcePluginStore::EnumerateTargets, sbtsv/ITsSbResourcePluginStoreEx::EnumerateTargets, termserv.itssbresourcepluginstore_enumeratetargets
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
 - ITsSbResourcePluginStore::EnumerateTargets
 - sbtsv/ITsSbResourcePluginStore::EnumerateTargets
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
 - ITsSbResourcePluginStore.EnumerateTargets
 - ITsSbResourcePluginStoreEx.EnumerateTargets
---

# ITsSbResourcePluginStore::EnumerateTargets


## -description

Returns an array that contains the specified targets that are present in the resource plug-in store.

## -parameters

### -param FarmName [in]

The farm name.

### -param EnvName [in]

The environment name.

### -param sortByFieldId [in]

Specifies sort order.

### -param sortyByPropName [in]

The property name to sort by if <i>sortByFieldId</i> is set to <b>TS_SB_SORT_BY_PROP</b>.

### -param pdwCount [in, out]

The number of targets retrieved.

### -param pVal [out]

Pointer to the retrieved <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> objects.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>