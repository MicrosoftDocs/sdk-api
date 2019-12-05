---
UID: NN:rometadataapi.IMetaDataTables
title: IMetaDataTables (rometadataapi.h)
description: Provides methods for the storage and retrieval of metadata information in tables.
old-location: winrt\imetadatatables.htm
tech.root: WinRT
ms.assetid: 30d06e87-93a2-4a9c-8843-4c42d7d9e3c8
ms.date: 12/05/2018
ms.keywords: IMetaDataTables, IMetaDataTables interface [Windows Runtime], IMetaDataTables interface [Windows Runtime],described, rometadataapi/IMetaDataTables, winrt.imetadatatables
ms.topic: interface
f1_keywords:
- rometadataapi/IMetaDataTables
dev_langs:
- c++
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
- rometadataapi.h
api_name:
- IMetaDataTables
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataTables interface


## -description


Provides methods for the storage and retrieval of metadata information in tables.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataTables</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMetaDataTables</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaDataTables</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getblob">GetBlob</a>
</td>
<td align="left" width="63%">
Gets a pointer to the binary large object (BLOB) at the specified column index.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getblobheapsize">GetBlobHeapSize</a>
</td>
<td align="left" width="63%">
A pointer to a pointer to the binary data retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getcodedtokeninfo">GetCodedTokenInfo</a>
</td>
<td align="left" width="63%">
Gets a pointer to an array of tokens associated with the specified row index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getcolumn">GetColumn</a>
</td>
<td align="left" width="63%">
Gets a pointer to the value contained in the cell of the specified column and row in the given table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getcolumninfo">GetColumnInfo</a>
</td>
<td align="left" width="63%">
Gets data about the specified column in the specified table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getguid">GetGuid</a>
</td>
<td align="left" width="63%">
Gets a GUID from the row at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getguidheapsize">GetGuidHeapSize</a>
</td>
<td align="left" width="63%">
Gets the size, in bytes, of the GUID heap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getnextblob">GetNextBlob</a>
</td>
<td align="left" width="63%">
Gets the index of the next binary large object (BLOB) in the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getnextguid">GetNextGuid</a>
</td>
<td align="left" width="63%">
Gets the index of the next GUID value in the current table column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getnextstring">GetNextString</a>
</td>
<td align="left" width="63%">
Gets the index of the next string in the current table column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getnextuserstring">GetNextUserString</a>
</td>
<td align="left" width="63%">
Gets the index of the row that contains the next hard-coded string in the current table column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getnumtables">GetNumTables</a>
</td>
<td align="left" width="63%">
Gets the number of tables in the scope of the current IMetaDataTables instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getrow">GetRow</a>
</td>
<td align="left" width="63%">
Gets the row at the specified row index, in the table at the specified table index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getstring">GetString</a>
</td>
<td align="left" width="63%">
Gets the string at the specified index from the table column in the current reference scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getstringheapsize">GetStringHeapSize</a>
</td>
<td align="left" width="63%">
Gets the size, in bytes, of the string heap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/hh870662(v=vs.85)">GetTableIndex</a>
</td>
<td align="left" width="63%">
Gets the index for the table referenced by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-gettableinfo">GetTableInfo</a>
</td>
<td align="left" width="63%">
Gets the name, row size, number of rows, number of columns, and key column index of the specified table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getuserstring">GetUserString</a>
</td>
<td align="left" width="63%">
Gets the hard-coded string at the specified index in the string column in the current scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatatables-getuserstringheapsize">GetUserStringHeapSize</a>
</td>
<td align="left" width="63%">
Gets the size, in bytes, of the user string heap.

</td>
</tr>
</table> 

