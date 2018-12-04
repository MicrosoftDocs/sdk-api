---
UID: NF:comadmin.ICatalogCollection.Populate
title: ICatalogCollection::Populate
author: windows-sdk-content
description: Populates the collection with data for all items contained in the collection.
old-location: cos\icatalogcollection_populate.htm
tech.root: cossdk
ms.assetid: 817f203c-ddc6-47bd-a946-2393067eca44
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ICatalogCollection interface [COM+],Populate method, ICatalogCollection.Populate, ICatalogCollection::Populate, Populate, Populate method [COM+], Populate method [COM+],ICatalogCollection interface, _cos_ICatalogCollection_Populate, comadmin/ICatalogCollection::Populate, cos.icatalogcollection_populate
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
 - ICatalogCollection.Populate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatalogCollection::Populate


## -description


Populates the collection with data for all items contained in the collection.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_OBJECTERRORS </b></dt>
</dl>
</td>
<td width="60%">
Errors occurred while accessing one or more objects.

</td>
</tr>
</table>
 




## -remarks



Call the <a href="https://msdn.microsoft.com/ae984eee-4a8d-48e5-839c-fa115fd4aeea">SaveChanges</a> method prior to calling the <b>Populate</b> method if you want to save pending changes. Unsaved changes made to the collection are lost when you call the <b>Populate</b> method.




## -see-also




<a href="https://msdn.microsoft.com/7c24ead4-d69f-467d-b3d8-a81adbc49a7b">ICatalogCollection</a>
 

 

