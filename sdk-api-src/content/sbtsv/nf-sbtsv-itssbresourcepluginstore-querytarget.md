---
UID: NF:sbtsv.ITsSbResourcePluginStore.QueryTarget
title: ITsSbResourcePluginStore::QueryTarget (sbtsv.h)
description: Returns the target that has the specified target name and farm name.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","QueryTarget method","ITsSbResourcePluginStore.QueryTarget","ITsSbResourcePluginStore::QueryTarget","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","QueryTarget method","ITsSbResourcePluginStoreEx::QueryTarget","QueryTarget","QueryTarget method [Remote Desktop Services]","QueryTarget method [Remote Desktop Services]","ITsSbResourcePluginStore interface","QueryTarget method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","sbtsv/ITsSbResourcePluginStore::QueryTarget","sbtsv/ITsSbResourcePluginStoreEx::QueryTarget","termserv.itssbresourcepluginstore_querytarget"]
old-location: termserv\itssbresourcepluginstore_querytarget.htm
tech.root: TermServ
ms.assetid: ef78c055-edf6-4f0c-b47c-836ef85310bf
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],QueryTarget method, ITsSbResourcePluginStore.QueryTarget, ITsSbResourcePluginStore::QueryTarget, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],QueryTarget method, ITsSbResourcePluginStoreEx::QueryTarget, QueryTarget, QueryTarget method [Remote Desktop Services], QueryTarget method [Remote Desktop Services],ITsSbResourcePluginStore interface, QueryTarget method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::QueryTarget, sbtsv/ITsSbResourcePluginStoreEx::QueryTarget, termserv.itssbresourcepluginstore_querytarget
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
 - ITsSbResourcePluginStore::QueryTarget
 - sbtsv/ITsSbResourcePluginStore::QueryTarget
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
 - ITsSbResourcePluginStore.QueryTarget
 - ITsSbResourcePluginStoreEx.QueryTarget
---

# ITsSbResourcePluginStore::QueryTarget


## -description

Returns the target that has the specified target name and farm name.

## -parameters

### -param TargetName [in]

The target name.

### -param FarmName [in]

The farm name. If this parameter is <b>NULL</b>, the method returns the first target it finds.

### -param ppTarget [out]

A pointer to a pointer to an  <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> target object. When you have finished using the object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A resource plug-in store can use this method to retrieve the target that has the specified target name and farm name. Unlike the global store, the resource plug-in store does not copy the target object retrieved because the resource plug-in owns the target object. Accordingly, if you modify the <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> object that is returned by this method, you are modifying the target object in    the            resource plug-in store.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>