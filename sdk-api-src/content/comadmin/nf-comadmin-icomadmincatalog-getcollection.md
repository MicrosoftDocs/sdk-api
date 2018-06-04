---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICOMAdminCatalog::GetCollection


## -description


Retrieves a top-level collection on the COM+ catalog.


## -parameters




### -param bstrCollName [in]

The name of the collection to be retrieved.


### -param ppCatalogCollection [out, retval]

The <a href="https://msdn.microsoft.com/7c24ead4-d69f-467d-b3d8-a81adbc49a7b">ICatalogCollection</a> interface for the collection.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



This method retrieves a top-level collection, such as the <a href="https://msdn.microsoft.com/library/windows/hardware/jj159048">Applications</a> collection, from the COM+ catalog. For related collections that are not top-level collections, such as <a href="https://msdn.microsoft.com/library/windows/hardware/dn922646">Components</a>, use the <a href="https://msdn.microsoft.com/4198f456-97fa-45b2-aa79-29ac506a8618">GetCollection</a> method available from the parent collection.

The catalog collection retrieved by <b>GetCollection</b> does not contain data from the catalog for items contained within the collection. Use the <a href="https://msdn.microsoft.com/817f203c-ddc6-47bd-a946-2393067eca44">Populate</a> method to read in data for items in the collection.

For a complete list of collections in the COM+ catalog, see <a href="https://msdn.microsoft.com/eed8ca97-39ad-4188-afc6-8670b5073fad">COM+ Administration Collections</a>.




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

