---
UID: NF:comadmin.ICatalogCollection.GetCollection
title: ICatalogCollection::GetCollection
author: windows-sdk-content
description: Retrieves a collection from the COM+ catalog that is related to the current collection.
old-location: cos\icatalogcollection_getcollection.htm
tech.root: cossdk
ms.assetid: 4198f456-97fa-45b2-aa79-29ac506a8618
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetCollection, GetCollection method [COM+], GetCollection method [COM+],ICatalogCollection interface, ICatalogCollection interface [COM+],GetCollection method, ICatalogCollection.GetCollection, ICatalogCollection::GetCollection, _cos_ICatalogCollection_GetCollection, comadmin/ICatalogCollection::GetCollection, cos.icatalogcollection_getcollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ComAdmin.h
api_name:
 - ICatalogCollection.GetCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatalogCollection::GetCollection


## -description


Retrieves a collection from the COM+ catalog that is related to the current collection.


## -parameters




### -param bstrCollName [in]

The name of the collection to be retrieved.


### -param varObjectKey [in]

The <a href="https://msdn.microsoft.com/1937cd5a-742f-4248-a4c2-0b39a03eed20">Key</a> property value of the parent item of the collection to be retrieved.


### -param ppCatalogCollection [out, retval]

The <a href="https://msdn.microsoft.com/7c24ead4-d69f-467d-b3d8-a81adbc49a7b">ICatalogCollection</a> interface for the retrieved collection.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



This method does not read in data for items in the retrieved collection from the catalog data store. Use the <a href="https://msdn.microsoft.com/817f203c-ddc6-47bd-a946-2393067eca44">Populate</a> method to read in data for items in the collection.




## -see-also




<a href="https://msdn.microsoft.com/7c24ead4-d69f-467d-b3d8-a81adbc49a7b">ICatalogCollection</a>
 

 

