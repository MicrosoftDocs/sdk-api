---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetTargetPropertyWithVersionCheck
title: ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck
author: windows-sdk-content
description: Sets the value of a property of a target.
old-location: termserv\itssbresourcepluginstore_settargetpropertywithversioncheck.htm
tech.root: termserv
ms.assetid: 51b5e267-da1a-4d83-81bc-0cf8fb525fa9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetTargetPropertyWithVersionCheck method, ITsSbResourcePluginStore.SetTargetPropertyWithVersionCheck, ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck, SetTargetPropertyWithVersionCheck, SetTargetPropertyWithVersionCheck method [Remote Desktop Services], SetTargetPropertyWithVersionCheck method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetTargetPropertyWithVersionCheck, termserv.itssbresourcepluginstore_settargetpropertywithversioncheck
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
 - ITsSbResourcePluginStore.SetTargetPropertyWithVersionCheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When  a target or environment object is updated, the version number in the database is  automatically updated. This method verifies that the version number of the object it has modified matches the internal version number in the database before attempting to save the updated object to the database.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a>



<a href="https://msdn.microsoft.com/11d03b69-a7d0-4930-ba9c-a9373706580c">SetTargetProperty</a>
 

 

