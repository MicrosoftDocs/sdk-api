---
UID: NF:sbtsv.ITsSbResourcePluginStore.RemoveEnvironmentFromStore
title: ITsSbResourcePluginStore::RemoveEnvironmentFromStore
author: windows-sdk-content
description: Removes the specified environment from the resource plug-in store.
old-location: termserv\itssbresourcepluginstore_removeenvironmentfromstore.htm
tech.root: termserv
ms.assetid: b1922ff2-6322-4868-ab7b-2f18386d7d08
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],RemoveEnvironmentFromStore method, ITsSbResourcePluginStore.RemoveEnvironmentFromStore, ITsSbResourcePluginStore::RemoveEnvironmentFromStore, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],RemoveEnvironmentFromStore method, ITsSbResourcePluginStoreEx::RemoveEnvironmentFromStore, RemoveEnvironmentFromStore, RemoveEnvironmentFromStore method [Remote Desktop Services], RemoveEnvironmentFromStore method [Remote Desktop Services],ITsSbResourcePluginStore interface, RemoveEnvironmentFromStore method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::RemoveEnvironmentFromStore, sbtsv/ITsSbResourcePluginStoreEx::RemoveEnvironmentFromStore, termserv.itssbresourcepluginstore_removeenvironmentfromstore
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITsSbResourcePluginStore.RemoveEnvironmentFromStore
 - ITsSbResourcePluginStoreEx.RemoveEnvironmentFromStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbResourcePluginStore::RemoveEnvironmentFromStore


## -description


Removes the specified environment from the resource plug-in store.


## -parameters




### -param EnvironmentName [in]

The name of the environment to remove.


### -param bIgnoreOwner [in, optional]

Set <b>TRUE</b> to ignore ownership of the environment; <b>FALSE</b> 
       otherwise.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This parameter is not supported before Windows Server 2016.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

