---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetEnvironmentPropertyWithVersionCheck
title: ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck (sbtsv.h)
description: Sets a property of an environment. (ITsSbResourcePluginStore.SetEnvironmentPropertyWithVersionCheck)
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","SetEnvironmentPropertyWithVersionCheck method","ITsSbResourcePluginStore.SetEnvironmentPropertyWithVersionCheck","ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck","SetEnvironmentPropertyWithVersionCheck","SetEnvironmentPropertyWithVersionCheck method [Remote Desktop Services]","SetEnvironmentPropertyWithVersionCheck method [Remote Desktop Services]","ITsSbResourcePluginStore interface","sbtsv/ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck","termserv.itssbresourcepluginstore_setenvironmentpropertywithversioncheck"]
old-location: termserv\itssbresourcepluginstore_setenvironmentpropertywithversioncheck.htm
tech.root: TermServ
ms.assetid: 9c4caee8-85fb-4d8f-9c5a-b82eea02a1d0
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetEnvironmentPropertyWithVersionCheck method, ITsSbResourcePluginStore.SetEnvironmentPropertyWithVersionCheck, ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck, SetEnvironmentPropertyWithVersionCheck, SetEnvironmentPropertyWithVersionCheck method [Remote Desktop Services], SetEnvironmentPropertyWithVersionCheck method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck, termserv.itssbresourcepluginstore_setenvironmentpropertywithversioncheck
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
 - ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck
 - sbtsv/ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck
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
 - ITsSbResourcePluginStore.SetEnvironmentPropertyWithVersionCheck
---

# ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck


## -description

Sets a property of an environment.

## -parameters

### -param pEnvironment [in]

A pointer to the environment.

### -param PropertyName [in]

The name of the property to set.

### -param pProperty [in]

A pointer to the value to set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When  a target or environment object is updated, the version number in the database is  automatically updated. This method verifies that the version number of the object it has modified matches the internal version number in the database before attempting to save the updated object to the database.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty">SetEnvironmentProperty</a>
