---
UID: NF:comadmin.ICOMAdminCatalog.GetCollectionByQuery
title: ICOMAdminCatalog::GetCollectionByQuery
author: windows-sdk-content
description: Retrieves a collection on the COM+ catalog given the key property values for all of its parent items.
old-location: cos\icomadmincatalog_getcollectionbyquery.htm
old-project: cossdk
ms.assetid: 6ec65e7c-fb67-4435-90cd-d17b8fbcbc84
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetCollectionByQuery, GetCollectionByQuery method [COM+], GetCollectionByQuery method [COM+],ICOMAdminCatalog interface, ICOMAdminCatalog interface [COM+],GetCollectionByQuery method, ICOMAdminCatalog.GetCollectionByQuery, ICOMAdminCatalog::GetCollectionByQuery, _cos_ICOMAdminCatalog_GetCollectionByQuery, comadmin/ICOMAdminCatalog::GetCollectionByQuery, cos.icomadmincatalog_getcollectionbyquery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.GetCollectionByQuery
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

The <a href="https://msdn.microsoft.com/en-us/library/ms683140(v=VS.85).aspx">ICatalogCollection</a> interface for the collection.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/ms679201(v=VS.85).aspx">ICatalogObject::Key</a> property value for an item is a GUID that serves to uniquely identify it in the COM+ catalog.

The <b>GetCollectionByQuery</b> method retrieves any collection on the catalog, given the key values for all of its parent items. However, with the <a href="https://msdn.microsoft.com/en-us/library/ms686530(v=VS.85).aspx">ErrorInfo</a>, <a href="https://msdn.microsoft.com/en-us/library/ms681735(v=VS.85).aspx">PropertyInfo</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms686925(v=VS.85).aspx">RelatedCollectionInfo</a> collections, this method behaves differently. If you specify any of these collections, <b>GetCollectionByQuery</b> always returns that named collection immediately relative to the <a href="https://msdn.microsoft.com/en-us/library/ms682277(v=VS.85).aspx">Root</a> collection.

To get the <a href="https://msdn.microsoft.com/en-us/library/ms686530(v=VS.85).aspx">ErrorInfo</a>, <a href="https://msdn.microsoft.com/en-us/library/ms681735(v=VS.85).aspx">PropertyInfo</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms686925(v=VS.85).aspx">RelatedCollectionInfo</a> collection that is relative to an arbitrary collection in the catalog and not relative to the <a href="https://msdn.microsoft.com/en-us/library/ms682277(v=VS.85).aspx">Root</a> collection, use the <a href="https://msdn.microsoft.com/en-us/library/ms680613(v=VS.85).aspx">GetCollection</a> method from the parent collection.

For a complete list of available collections, see <a href="https://msdn.microsoft.com/en-us/library/ms687763(v=VS.85).aspx">COM+ Administration Collections</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee309561(v=VS.85).aspx">ICOMAdminCatalog</a>
 

 

