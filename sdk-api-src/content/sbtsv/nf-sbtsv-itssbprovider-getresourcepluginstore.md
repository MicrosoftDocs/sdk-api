---
UID: NF:sbtsv.ITsSbProvider.GetResourcePluginStore
title: ITsSbProvider::GetResourcePluginStore
author: windows-sdk-content
description: Retrieves an ITsSbResourcePluginStore instance of the resource plug-in store.
old-location: termserv\itssbprovider_getresourcepluginstore.htm
tech.root: termserv
ms.assetid: 9e4d5b1d-100e-49e1-b1b5-4b126683c329
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetResourcePluginStore, GetResourcePluginStore method [Remote Desktop Services], GetResourcePluginStore method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],GetResourcePluginStore method, ITsSbProvider.GetResourcePluginStore, ITsSbProvider::GetResourcePluginStore, sbtsv/ITsSbProvider::GetResourcePluginStore, termserv.itssbprovider_getresourcepluginstore
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
 - ITsSbProvider.GetResourcePluginStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbProvider::GetResourcePluginStore


## -description


Retrieves an <a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a> instance of the resource plug-in store.

Plug-ins can call this method if they have access to the <a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a> and <a href="https://msdn.microsoft.com/a5223902-2e2a-4fba-ae05-240824a140ac">ITsSbResourcePlugin</a> objects that own the store. This method returns an instance of the resource plug-in store.


## -parameters




### -param ppStore [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a> resource plug-in store object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.




## -see-also




<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>



<a href="https://msdn.microsoft.com/a5223902-2e2a-4fba-ae05-240824a140ac">ITsSbResourcePlugin</a>



<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>
 

 

