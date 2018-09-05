---
UID: NF:comadmin.ICatalogCollection.PopulateByKey
title: ICatalogCollection::PopulateByKey
author: windows-sdk-content
description: Populates a selected list of items in the collection from the COM+ catalog, based on the specified keys.
old-location: cos\icatalogcollection_populatebykey.htm
old-project: cossdk
ms.assetid: 57329c32-2852-47ff-bf8c-dbb63f69841f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICatalogCollection interface [COM+],PopulateByKey method, ICatalogCollection.PopulateByKey, ICatalogCollection::PopulateByKey, PopulateByKey, PopulateByKey method [COM+], PopulateByKey method [COM+],ICatalogCollection interface, _cos_ICatalogCollection_PopulateByKey, comadmin/ICatalogCollection::PopulateByKey, cos.icatalogcollection_populatebykey
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
 - ICatalogCollection.PopulateByKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatalogCollection::PopulateByKey


## -description


Populates a selected list of items in the collection from the COM+ catalog, based on the specified keys.


## -parameters




### -param psaKeys [in]

The <a href="https://msdn.microsoft.com/1937cd5a-742f-4248-a4c2-0b39a03eed20">Key</a> property value of the objects for which data is to be read.


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



Call the <a href="https://msdn.microsoft.com/ae984eee-4a8d-48e5-839c-fa115fd4aeea">SaveChanges</a> method prior to calling <b>PopulateByKey</b> if you want to save pending changes. Unsaved changes made to the collection are lost when you call <b>PopulateByKey</b>.




## -see-also




<a href="https://msdn.microsoft.com/7c24ead4-d69f-467d-b3d8-a81adbc49a7b">ICatalogCollection</a>
 

 

