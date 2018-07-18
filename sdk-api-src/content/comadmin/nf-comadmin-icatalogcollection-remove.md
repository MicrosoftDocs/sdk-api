---
UID: NF:comadmin.ICatalogCollection.Remove
title: ICatalogCollection::Remove
author: windows-sdk-content
description: Removes an item from the collection, given its index, and re-indexes the items with higher index values.
old-location: cos\icatalogcollection_remove.htm
old-project: cossdk
ms.assetid: 984f60b1-0963-482c-90a3-563e8699f73d
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ICatalogCollection interface [COM+],Remove method, ICatalogCollection.Remove, ICatalogCollection::Remove, Remove, Remove method [COM+], Remove method [COM+],ICatalogCollection interface, _cos_ICatalogCollection_Remove, comadmin/ICatalogCollection::Remove, cos.icatalogcollection_remove
ms.prod: windows
ms.technology: windows-sdk
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
 - ICatalogCollection.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatalogCollection::Remove


## -description


Removes an item from the collection, given its index, and re-indexes the items with higher index values.


## -parameters




### -param lIndex [in]

The zero-based index of the item to be removed.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The <a href="https://msdn.microsoft.com/eda0812f-a0e4-4239-87b5-c252e9e3492c">RemoveEnabled</a> property indicates whether the collection supports this method.

When an object is removed, the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a> property is decremented to reflect the change.

These changes are not reflected in the COM+ catalog data store until you call <a href="https://msdn.microsoft.com/ae984eee-4a8d-48e5-839c-fa115fd4aeea">SaveChanges</a>.




## -see-also




<a href="https://msdn.microsoft.com/7c24ead4-d69f-467d-b3d8-a81adbc49a7b">ICatalogCollection</a>
 

 

