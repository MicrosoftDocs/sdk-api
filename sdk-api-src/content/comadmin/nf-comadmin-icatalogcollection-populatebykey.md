---
UID: NF:comadmin.ICatalogCollection.PopulateByKey
title: ICatalogCollection::PopulateByKey (comadmin.h)
description: Populates a selected list of items in the collection from the COM+ catalog, based on the specified keys.
helpviewer_keywords: ["ICatalogCollection interface [COM+]","PopulateByKey method","ICatalogCollection.PopulateByKey","ICatalogCollection::PopulateByKey","PopulateByKey","PopulateByKey method [COM+]","PopulateByKey method [COM+]","ICatalogCollection interface","_cos_ICatalogCollection_PopulateByKey","comadmin/ICatalogCollection::PopulateByKey","cos.icatalogcollection_populatebykey"]
old-location: cos\icatalogcollection_populatebykey.htm
tech.root: cos
ms.assetid: 57329c32-2852-47ff-bf8c-dbb63f69841f
ms.date: 12/05/2018
ms.keywords: ICatalogCollection interface [COM+],PopulateByKey method, ICatalogCollection.PopulateByKey, ICatalogCollection::PopulateByKey, PopulateByKey, PopulateByKey method [COM+], PopulateByKey method [COM+],ICatalogCollection interface, _cos_ICatalogCollection_PopulateByKey, comadmin/ICatalogCollection::PopulateByKey, cos.icatalogcollection_populatebykey
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
 - ICatalogCollection::PopulateByKey
 - comadmin/ICatalogCollection::PopulateByKey
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
 - ICatalogCollection.PopulateByKey
---

# ICatalogCollection::PopulateByKey


## -description

Populates a selected list of items in the collection from the COM+ catalog, based on the specified keys.

## -parameters

### -param psaKeys [in]

The <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_key">Key</a> property value of the objects for which data is to be read.

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

Call the <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-savechanges">SaveChanges</a> method prior to calling <b>PopulateByKey</b> if you want to save pending changes. Unsaved changes made to the collection are lost when you call <b>PopulateByKey</b>.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a>