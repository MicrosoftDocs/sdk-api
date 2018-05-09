---
UID: NF:comadmin.ICOMAdminCatalog.GetCollectionByQuery
title: ICOMAdminCatalog::GetCollectionByQuery
author: windows-driver-content
description: Retrieves a collection on the COM+ catalog given the key property values for all of its parent items.
old-location: cos\icomadmincatalog_getcollectionbyquery.htm
old-project: cossdk
ms.assetid: 6ec65e7c-fb67-4435-90cd-d17b8fbcbc84
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetCollectionByQuery, GetCollectionByQuery method [COM+], GetCollectionByQuery method [COM+],ICOMAdminCatalog interface, ICOMAdminCatalog interface [COM+],GetCollectionByQuery method, ICOMAdminCatalog.GetCollectionByQuery, ICOMAdminCatalog::GetCollectionByQuery, _cos_ICOMAdminCatalog_GetCollectionByQuery, comadmin/ICOMAdminCatalog::GetCollectionByQuery, cos.icomadmincatalog_getcollectionbyquery
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
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICOMAdminCatalog.GetCollectionByQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog::GetCollectionByQuery


## -description


Retrieves a collection on the COM+ catalog given the key property values for all of its parent items.


## -parameters




### -param bstrCollName [in]

The name of the collection to be retrieved.


### -param ppsaVarQuery [in]

A reference to an array consisting of key property values for all parent items of the collection to be retrieved.


### -param ppCatalogCollection [out, retval]

The <a href="https://msdn.microsoft.com/7c24ead4-d69f-467d-b3d8-a81adbc49a7b">ICatalogCollection</a> interface for the collection.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The <a href="https://msdn.microsoft.com/1937cd5a-742f-4248-a4c2-0b39a03eed20">ICatalogObject::Key</a> property value for an item is a GUID that serves to uniquely identify it in the COM+ catalog.

The <b>GetCollectionByQuery</b> method retrieves any collection on the catalog, given the key values for all of its parent items. However, with the <a href="https://msdn.microsoft.com/cf612fc4-55dd-4706-8c41-2654ca922b9a">ErrorInfo</a>, <a href="https://msdn.microsoft.com/5e3963c0-6769-4b5b-8636-2d8c98a8776b">PropertyInfo</a>, and <a href="https://msdn.microsoft.com/daea5b23-6a13-46f4-89c8-0d93b614311e">RelatedCollectionInfo</a> collections, this method behaves differently. If you specify any of these collections, <b>GetCollectionByQuery</b> always returns that named collection immediately relative to the <a href="https://msdn.microsoft.com/library/windows/hardware/mt484162">Root</a> collection.

To get the <a href="https://msdn.microsoft.com/cf612fc4-55dd-4706-8c41-2654ca922b9a">ErrorInfo</a>, <a href="https://msdn.microsoft.com/5e3963c0-6769-4b5b-8636-2d8c98a8776b">PropertyInfo</a>, or <a href="https://msdn.microsoft.com/daea5b23-6a13-46f4-89c8-0d93b614311e">RelatedCollectionInfo</a> collection that is relative to an arbitrary collection in the catalog and not relative to the <a href="https://msdn.microsoft.com/library/windows/hardware/mt484162">Root</a> collection, use the <a href="https://msdn.microsoft.com/4198f456-97fa-45b2-aa79-29ac506a8618">GetCollection</a> method from the parent collection.

For a complete list of available collections, see <a href="https://msdn.microsoft.com/eed8ca97-39ad-4188-afc6-8670b5073fad">COM+ Administration Collections</a>.




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

