---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetTargetProperty
title: ITsSbResourcePluginStore::SetTargetProperty (sbtsv.h)
description: Sets the value of a property of a target.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","SetTargetProperty method","ITsSbResourcePluginStore.SetTargetProperty","ITsSbResourcePluginStore::SetTargetProperty","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","SetTargetProperty method","ITsSbResourcePluginStoreEx::SetTargetProperty","SetTargetProperty","SetTargetProperty method [Remote Desktop Services]","SetTargetProperty method [Remote Desktop Services]","ITsSbResourcePluginStore interface","SetTargetProperty method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","sbtsv/ITsSbResourcePluginStore::SetTargetProperty","sbtsv/ITsSbResourcePluginStoreEx::SetTargetProperty","termserv.itssbresourcepluginstore_settargetproperty"]
old-location: termserv\itssbresourcepluginstore_settargetproperty.htm
tech.root: TermServ
ms.assetid: 11d03b69-a7d0-4930-ba9c-a9373706580c
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetTargetProperty method, ITsSbResourcePluginStore.SetTargetProperty, ITsSbResourcePluginStore::SetTargetProperty, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],SetTargetProperty method, ITsSbResourcePluginStoreEx::SetTargetProperty, SetTargetProperty, SetTargetProperty method [Remote Desktop Services], SetTargetProperty method [Remote Desktop Services],ITsSbResourcePluginStore interface, SetTargetProperty method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::SetTargetProperty, sbtsv/ITsSbResourcePluginStoreEx::SetTargetProperty, termserv.itssbresourcepluginstore_settargetproperty
f1_keywords:
- sbtsv/ITsSbResourcePluginStore.SetTargetProperty
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sbtsv.h
api_name:
- ITsSbResourcePluginStore.SetTargetProperty
- ITsSbResourcePluginStoreEx.SetTargetProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbResourcePluginStore::SetTargetProperty


## -description


Sets the value of a  property of a target.


## -parameters




### -param TargetName [in]

The name of the target.


### -param PropertyName [in]

The name of the property.


### -param pProperty [in]

A pointer to the value to set.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck">SetTargetPropertyWithVersionCheck</a>
 

 

