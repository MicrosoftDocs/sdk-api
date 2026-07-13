---
UID: NF:comadmin.ICatalogCollection.Populate
title: ICatalogCollection::Populate (comadmin.h)
description: Populates the collection with data for all items contained in the collection.
helpviewer_keywords: ["ICatalogCollection interface [COM+]","Populate method","ICatalogCollection.Populate","ICatalogCollection::Populate","Populate","Populate method [COM+]","Populate method [COM+]","ICatalogCollection interface","_cos_ICatalogCollection_Populate","comadmin/ICatalogCollection::Populate","cos.icatalogcollection_populate"]
old-location: cos\icatalogcollection_populate.htm
tech.root: cos
ms.assetid: 817f203c-ddc6-47bd-a946-2393067eca44
ms.date: 12/05/2018
ms.keywords: ICatalogCollection interface [COM+],Populate method, ICatalogCollection.Populate, ICatalogCollection::Populate, Populate, Populate method [COM+], Populate method [COM+],ICatalogCollection interface, _cos_ICatalogCollection_Populate, comadmin/ICatalogCollection::Populate, cos.icatalogcollection_populate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICatalogCollection::Populate
 - comadmin/ICatalogCollection::Populate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICatalogCollection.Populate
---

# ICatalogCollection::Populate


## -description

Populates the collection with data for all items contained in the collection.



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

Call the <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-savechanges">SaveChanges</a> method prior to calling the <b>Populate</b> method if you want to save pending changes. Unsaved changes made to the collection are lost when you call the <b>Populate</b> method.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a>
