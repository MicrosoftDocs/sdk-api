---
UID: NF:comadmin.ICatalogCollection.PopulateByQuery
title: ICatalogCollection::PopulateByQuery (comadmin.h)
description: Reserved for future use. (ICatalogCollection.PopulateByQuery)
helpviewer_keywords: ["ICatalogCollection interface [COM+]","PopulateByQuery method","ICatalogCollection.PopulateByQuery","ICatalogCollection::PopulateByQuery","PopulateByQuery","PopulateByQuery method [COM+]","PopulateByQuery method [COM+]","ICatalogCollection interface","_cos_ICatalogCollection_PopulateByQuery","comadmin/ICatalogCollection::PopulateByQuery","cos.icatalogcollection_populatebyquery"]
old-location: cos\icatalogcollection_populatebyquery.htm
tech.root: cos
ms.assetid: 30e4bb16-f99f-4541-a70a-64eb285df7b6
ms.date: 12/05/2018
ms.keywords: ICatalogCollection interface [COM+],PopulateByQuery method, ICatalogCollection.PopulateByQuery, ICatalogCollection::PopulateByQuery, PopulateByQuery, PopulateByQuery method [COM+], PopulateByQuery method [COM+],ICatalogCollection interface, _cos_ICatalogCollection_PopulateByQuery, comadmin/ICatalogCollection::PopulateByQuery, cos.icatalogcollection_populatebyquery
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
 - ICatalogCollection::PopulateByQuery
 - comadmin/ICatalogCollection::PopulateByQuery
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
 - ICatalogCollection.PopulateByQuery
---

# ICatalogCollection::PopulateByQuery


## -description

Reserved for future use.

## -parameters

### -param bstrQueryString [in]

### -param lQueryType [in]

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

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a>
