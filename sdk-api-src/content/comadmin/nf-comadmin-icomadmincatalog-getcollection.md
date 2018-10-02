---
UID: NF:comadmin.ICOMAdminCatalog.GetCollection
title: ICOMAdminCatalog::GetCollection
author: windows-sdk-content
description: Retrieves a top-level collection on the COM+ catalog.
old-location: cos\icomadmincatalog_getcollection.htm
tech.root: cossdk
ms.assetid: 6f01a7a7-d8f3-470f-8eb3-aa698b353af1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCollection, GetCollection method [COM+], GetCollection method [COM+],ICOMAdminCatalog interface, ICOMAdminCatalog interface [COM+],GetCollection method, ICOMAdminCatalog.GetCollection, ICOMAdminCatalog::GetCollection, _cos_ICOMAdminCatalog_GetCollection, comadmin/ICOMAdminCatalog::GetCollection, cos.icomadmincatalog_getcollection
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
 - ICOMAdminCatalog.GetCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This method retrieves a top-level collection, such as the <a href="https://msdn.microsoft.com/c0c46592-5282-412d-8f54-67637be8218a">Applications</a> collection, from the COM+ catalog. For related collections that are not top-level collections, such as <a href="https://msdn.microsoft.com/f502ba60-b2b1-4556-8f91-22a474e60e0d">Components</a>, use the <a href="https://msdn.microsoft.com/4198f456-97fa-45b2-aa79-29ac506a8618">GetCollection</a> method available from the parent collection.

The catalog collection retrieved by <b>GetCollection</b> does not contain data from the catalog for items contained within the collection. Use the <a href="https://msdn.microsoft.com/817f203c-ddc6-47bd-a946-2393067eca44">Populate</a> method to read in data for items in the collection.

For a complete list of collections in the COM+ catalog, see <a href="https://msdn.microsoft.com/eed8ca97-39ad-4188-afc6-8670b5073fad">COM+ Administration Collections</a>.




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

