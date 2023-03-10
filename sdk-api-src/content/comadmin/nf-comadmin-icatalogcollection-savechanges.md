---
UID: NF:comadmin.ICatalogCollection.SaveChanges
title: ICatalogCollection::SaveChanges (comadmin.h)
description: Saves all pending changes made to the collection and the items it contains to the COM+ catalog data store.
helpviewer_keywords: ["ICatalogCollection interface [COM+]","SaveChanges method","ICatalogCollection.SaveChanges","ICatalogCollection::SaveChanges","SaveChanges","SaveChanges method [COM+]","SaveChanges method [COM+]","ICatalogCollection interface","_cos_ICatalogCollection_SaveChanges","comadmin/ICatalogCollection::SaveChanges","cos.icatalogcollection_savechanges"]
old-location: cos\icatalogcollection_savechanges.htm
tech.root: cos
ms.assetid: ae984eee-4a8d-48e5-839c-fa115fd4aeea
ms.date: 12/05/2018
ms.keywords: ICatalogCollection interface [COM+],SaveChanges method, ICatalogCollection.SaveChanges, ICatalogCollection::SaveChanges, SaveChanges, SaveChanges method [COM+], SaveChanges method [COM+],ICatalogCollection interface, _cos_ICatalogCollection_SaveChanges, comadmin/ICatalogCollection::SaveChanges, cos.icatalogcollection_savechanges
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
 - ICatalogCollection::SaveChanges
 - comadmin/ICatalogCollection::SaveChanges
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
 - ICatalogCollection.SaveChanges
---

# ICatalogCollection::SaveChanges


## -description

Saves all pending changes made to the collection and the items it contains to the COM+ catalog data store.

## -parameters

### -param pcChanges [out, retval]

The number of changes to the collection that are being attempted; if no changes are pending, the value is zero. If some changes fail, this returned value does not reflect the failure; it is still the number of changes attempted.

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

For a given item, <b>SaveChanges</b> writes all properties to the catalog at the same time. That is, if the write succeeds for that item, all properties as they are set in the item you held are reflected in the catalog. The rule with multiple parties writing the same item in a collection is that the last writer wins entirely. There are no partial updates.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a>