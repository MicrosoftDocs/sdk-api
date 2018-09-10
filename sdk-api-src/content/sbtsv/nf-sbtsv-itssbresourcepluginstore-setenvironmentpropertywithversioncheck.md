---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetEnvironmentPropertyWithVersionCheck
title: ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck
author: windows-sdk-content
description: Sets a property of an environment.
old-location: termserv\itssbresourcepluginstore_setenvironmentpropertywithversioncheck.htm
tech.root: termserv
ms.assetid: 9c4caee8-85fb-4d8f-9c5a-b82eea02a1d0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetEnvironmentPropertyWithVersionCheck method, ITsSbResourcePluginStore.SetEnvironmentPropertyWithVersionCheck, ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck, SetEnvironmentPropertyWithVersionCheck, SetEnvironmentPropertyWithVersionCheck method [Remote Desktop Services], SetEnvironmentPropertyWithVersionCheck method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetEnvironmentPropertyWithVersionCheck, termserv.itssbresourcepluginstore_setenvironmentpropertywithversioncheck
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.SetEnvironmentPropertyWithVersionCheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When  a target or environment object is updated, the version number in the database is  automatically updated. This method verifies that the version number of the object it has modified matches the internal version number in the database before attempting to save the updated object to the database.




## -see-also




<a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a>



<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/a120ff15-2d78-4bca-b470-0eb03933a4d9">SetEnvironmentProperty</a>
 

 

