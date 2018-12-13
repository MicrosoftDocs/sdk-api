---
UID: NF:sbtsv.ITsSbResourcePluginStore.AddEnvironmentToStore
title: ITsSbResourcePluginStore::AddEnvironmentToStore
author: windows-sdk-content
description: Adds an environment to the resource plug-in store.
old-location: termserv\itssbresourcepluginstore_addenvironmenttostore.htm
tech.root: TermServ
ms.assetid: 5f1d995b-10de-4754-9160-fb93a9d8f263
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddEnvironmentToStore, AddEnvironmentToStore method [Remote Desktop Services], AddEnvironmentToStore method [Remote Desktop Services],ITsSbResourcePluginStore interface, AddEnvironmentToStore method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],AddEnvironmentToStore method, ITsSbResourcePluginStore.AddEnvironmentToStore, ITsSbResourcePluginStore::AddEnvironmentToStore, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],AddEnvironmentToStore method, ITsSbResourcePluginStoreEx::AddEnvironmentToStore, sbtsv/ITsSbResourcePluginStore::AddEnvironmentToStore, sbtsv/ITsSbResourcePluginStoreEx::AddEnvironmentToStore, termserv.itssbresourcepluginstore_addenvironmenttostore
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
 - ITsSbResourcePluginStore.AddEnvironmentToStore
 - ITsSbResourcePluginStoreEx.AddEnvironmentToStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbResourcePluginStore::AddEnvironmentToStore


## -description


Adds an environment to the resource plug-in store.


## -parameters




### -param pEnvironment [in]

A pointer to an <a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a> environment object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Resource plug-ins can use this  method to add an environment to the resource plug-in store.




## -see-also




<a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a>



<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

