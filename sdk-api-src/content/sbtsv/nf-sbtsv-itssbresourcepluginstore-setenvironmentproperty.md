---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetEnvironmentProperty
title: ITsSbResourcePluginStore::SetEnvironmentProperty (sbtsv.h)
description: Sets a property of an environment. (ITsSbResourcePluginStoreEx.SetEnvironmentProperty)
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","SetEnvironmentProperty method","ITsSbResourcePluginStore.SetEnvironmentProperty","ITsSbResourcePluginStore::SetEnvironmentProperty","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","SetEnvironmentProperty method","ITsSbResourcePluginStoreEx::SetEnvironmentProperty","SetEnvironmentProperty","SetEnvironmentProperty method [Remote Desktop Services]","SetEnvironmentProperty method [Remote Desktop Services]","ITsSbResourcePluginStore interface","SetEnvironmentProperty method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","sbtsv/ITsSbResourcePluginStore::SetEnvironmentProperty","sbtsv/ITsSbResourcePluginStoreEx::SetEnvironmentProperty","termserv.itssbresourcepluginstore_setenvironmentproperty"]
old-location: termserv\itssbresourcepluginstore_setenvironmentproperty.htm
tech.root: TermServ
ms.assetid: a120ff15-2d78-4bca-b470-0eb03933a4d9
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetEnvironmentProperty method, ITsSbResourcePluginStore.SetEnvironmentProperty, ITsSbResourcePluginStore::SetEnvironmentProperty, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],SetEnvironmentProperty method, ITsSbResourcePluginStoreEx::SetEnvironmentProperty, SetEnvironmentProperty, SetEnvironmentProperty method [Remote Desktop Services], SetEnvironmentProperty method [Remote Desktop Services],ITsSbResourcePluginStore interface, SetEnvironmentProperty method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::SetEnvironmentProperty, sbtsv/ITsSbResourcePluginStoreEx::SetEnvironmentProperty, termserv.itssbresourcepluginstore_setenvironmentproperty
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
 - ITsSbResourcePluginStore::SetEnvironmentProperty
 - sbtsv/ITsSbResourcePluginStore::SetEnvironmentProperty
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
 - ITsSbResourcePluginStore.SetEnvironmentProperty
 - ITsSbResourcePluginStoreEx.SetEnvironmentProperty
---

# ITsSbResourcePluginStore::SetEnvironmentProperty


## -description

Sets a property of an environment.

## -parameters

### -param EnvironmentName [in]

The name of the environment.

### -param PropertyName [in]

The name of the property to set.

### -param pProperty [in]

A pointer to the value to set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>



<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck">SetEnvironmentPropertyWithVersionCheck</a>
