---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetTargetPropertyWithVersionCheck
title: ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck (sbtsv.h)
description: Sets the value of a property of a target. (ITsSbResourcePluginStore.SetTargetPropertyWithVersionCheck)
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","SetTargetPropertyWithVersionCheck method","ITsSbResourcePluginStore.SetTargetPropertyWithVersionCheck","ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck","SetTargetPropertyWithVersionCheck","SetTargetPropertyWithVersionCheck method [Remote Desktop Services]","SetTargetPropertyWithVersionCheck method [Remote Desktop Services]","ITsSbResourcePluginStore interface","sbtsv/ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck","termserv.itssbresourcepluginstore_settargetpropertywithversioncheck"]
old-location: termserv\itssbresourcepluginstore_settargetpropertywithversioncheck.htm
tech.root: TermServ
ms.assetid: 51b5e267-da1a-4d83-81bc-0cf8fb525fa9
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetTargetPropertyWithVersionCheck method, ITsSbResourcePluginStore.SetTargetPropertyWithVersionCheck, ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck, SetTargetPropertyWithVersionCheck, SetTargetPropertyWithVersionCheck method [Remote Desktop Services], SetTargetPropertyWithVersionCheck method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck, termserv.itssbresourcepluginstore_settargetpropertywithversioncheck
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck
 - sbtsv/ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck
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
 - ITsSbResourcePluginStore.SetTargetPropertyWithVersionCheck
---

# ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck


## -description

Sets the value of a property of a target.

## -parameters

### -param pTarget [in]

A pointer to the target.

### -param PropertyName [in]

The name of the property.

### -param pProperty [in]

A pointer to the value to set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When  a target or environment object is updated, the version number in the database is  automatically updated. This method verifies that the version number of the object it has modified matches the internal version number in the database before attempting to save the updated object to the database.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>



<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty">SetTargetProperty</a>
