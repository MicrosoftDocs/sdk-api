---
UID: NF:ntquery.CIRestrictionToFullTree
title: CIRestrictionToFullTree function (ntquery.h)
description: Converts a query restriction tree with columns, sort columns, and grouping columns to a DBCOMMANDTREE structure.
helpviewer_keywords: ["CIRestrictionToFullTree","CIRestrictionToFullTree function [Indexing Service]","_idxs_CIRestrictionToFullTree","indexsrv.cirestrictiontofulltree","ntquery/CIRestrictionToFullTree"]
old-location: indexsrv\cirestrictiontofulltree.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_2c2t.htm
ms.date: 12/05/2018
ms.keywords: CIRestrictionToFullTree, CIRestrictionToFullTree function [Indexing Service], _idxs_CIRestrictionToFullTree, indexsrv.cirestrictiontofulltree, ntquery/CIRestrictionToFullTree
f1_keywords:
- ntquery/CIRestrictionToFullTree
dev_langs:
- c++
req.header: ntquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntquery.lib
req.dll: Ntquery.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ntquery.dll
api_name:
- CIRestrictionToFullTree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CIRestrictionToFullTree function


## -description


> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Converts a query restriction tree with columns, sort columns, and grouping columns to a <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure.


## -parameters




### -param pTree

A pointer to a <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure that is the top node defining a <b>SELECT</b> tree for a query.


### -param pwszColumns

A pointer to a null-terminated string that specifies a comma separated list of column names returned in the query results. These columns can be bound by OLE DB accessors and are used to create the <b>PROJECT</b> part of the full tree.


### -param pwszSortColumns

A pointer to a null-terminated string that contains a comma-separated list of column names that specify the sort order for the query results. A sort direction can be appended to each column name. Use [d] for descending, and [a] for ascending. If no sort order is specified, ascending is the default. This parameter can be <b>NULL</b> for no sort order. These columns are used to create the <b>SORT</b> part of the full tree.


### -param pwszGroupings

A pointer to a null-terminated string that contains a grouping specification made up of a type (currently only [unique] is supported), a property name, and a sort order ([a] for ascending or [d] for descending). In a unique grouping, unique values of the column set form the individual categories. This parameter is optional.

The syntax for the unique grouping term is: 

unique <i>fname</i> [ {[a]|[d]} ] [ , <i>fname2</i> {[a]|[d]} ... ]

where <i>fname</i> and <i>fname2</i> are the assigned friendly names.

Column names separated by a plus sign (+) are grouped in individual categories, and column names following a comma (,) are grouped together into subgroups of the preceding grouping.


### -param ppTree

A pointer to an output variable that receives a pointer to a <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure. This parameter cannot be <b>NULL</b>.


### -param cProperties

The number of properties in the <i>pProperties</i> array, or zero if <i>pProperties</i> is <b>NULL</b>.


### -param pReserved

A pointer to an array of properties that can be referred to by a friendly name in the <i>pwszColumns</i>, <i>pwszSortColumns</i>, and <i>pwszGroupings</i> parameters. Column names in the <b>wcsFriendlyName</b> member of each <a href="/windows/desktop/api/ntquery/ns-ntquery-cipropertydef">CIPROPERTYDEF</a> structure must be specified in uppercase. This parameter can be <b>NULL</b> if no properties are being defined and if <i>cProperties</i> is zero. Indexing Service's built-in properties do not need to be defined to be used. It is an error to define a property with the same friendly name as that of a built-in property.


### -param LocaleID

The locale identifier (LCID) used when converting properties.


## -returns



This function can return one of these values.

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
The operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The function encountered an invalid handle, probably due to a low-memory situation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The function received an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function did not have sufficient memory or other resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unknown error has occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="/windows/desktop/api/ntquery/ns-ntquery-cipropertydef">CIPROPERTYDEF</a>



<a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a>
 

 