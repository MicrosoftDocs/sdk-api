---
UID: NF:sbtsv.ITsSbProvider.GetInstanceOfGlobalStore
title: ITsSbProvider::GetInstanceOfGlobalStore
author: windows-sdk-content
description: Retrieves an ITsSbGlobalStore instance of the global store object.
old-location: termserv\itssbprovider_getinstanceofglobalstore.htm
old-project: TermServ
ms.assetid: e6c83775-56e7-4342-a26a-418f472e190f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetInstanceOfGlobalStore, GetInstanceOfGlobalStore method [Remote Desktop Services], GetInstanceOfGlobalStore method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],GetInstanceOfGlobalStore method, ITsSbProvider.GetInstanceOfGlobalStore, ITsSbProvider::GetInstanceOfGlobalStore, sbtsv/ITsSbProvider::GetInstanceOfGlobalStore, termserv.itssbprovider_getinstanceofglobalstore
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvider.GetInstanceOfGlobalStore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbProvider::GetInstanceOfGlobalStore


## -description


Retrieves an <a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a> instance of the global store object.

Plug-ins can use this method to get an instance of the global store object. The global store object is designed for use by filter plug-ins that do not have access to the resource plug-in store.


## -parameters




### -param ppGlobalStore [out]

A pointer to a pointer to a global store object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a>



<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>
 

 

