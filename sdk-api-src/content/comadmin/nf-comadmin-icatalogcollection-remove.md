---
UID: NF:comadmin.ICatalogCollection.Remove
title: ICatalogCollection::Remove (comadmin.h)
author: windows-sdk-content
description: Removes an item from the collection, given its index, and re-indexes the items with higher index values.
old-location: cos\icatalogcollection_remove.htm
tech.root: cossdk
ms.assetid: 984f60b1-0963-482c-90a3-563e8699f73d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICatalogCollection interface [COM+],Remove method, ICatalogCollection.Remove, ICatalogCollection::Remove, Remove, Remove method [COM+], Remove method [COM+],ICatalogCollection interface, _cos_ICatalogCollection_Remove, comadmin/ICatalogCollection::Remove, cos.icatalogcollection_remove
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
 - ICatalogCollection.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



The <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_removeenabled">RemoveEnabled</a> property indicates whether the collection supports this method.

When an object is removed, the <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_count">Count</a> property is decremented to reflect the change.

These changes are not reflected in the COM+ catalog data store until you call <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-savechanges">SaveChanges</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a>
 

 

