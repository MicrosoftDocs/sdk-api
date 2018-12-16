---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetEnvironmentProperty
title: ITsSbResourcePluginStore::SetEnvironmentProperty
author: windows-sdk-content
description: Sets a property of an environment.
old-location: termserv\itssbresourcepluginstore_setenvironmentproperty.htm
tech.root: TermServ
ms.assetid: a120ff15-2d78-4bca-b470-0eb03933a4d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetEnvironmentProperty method, ITsSbResourcePluginStore.SetEnvironmentProperty, ITsSbResourcePluginStore::SetEnvironmentProperty, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],SetEnvironmentProperty method, ITsSbResourcePluginStoreEx::SetEnvironmentProperty, SetEnvironmentProperty, SetEnvironmentProperty method [Remote Desktop Services], SetEnvironmentProperty method [Remote Desktop Services],ITsSbResourcePluginStore interface, SetEnvironmentProperty method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::SetEnvironmentProperty, sbtsv/ITsSbResourcePluginStoreEx::SetEnvironmentProperty, termserv.itssbresourcepluginstore_setenvironmentproperty
ms.topic: method
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
 - ITsSbResourcePluginStore.SetEnvironmentProperty
 - ITsSbResourcePluginStoreEx.SetEnvironmentProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a>



<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>



<a href="https://msdn.microsoft.com/9c4caee8-85fb-4d8f-9c5a-b82eea02a1d0">SetEnvironmentPropertyWithVersionCheck</a>
 

 

