---
UID: NN:rometadataapi.IMetaDataTables
title: IMetaDataTables (rometadataapi.h)
author: windows-sdk-content
description: Provides methods for the storage and retrieval of metadata information in tables.
old-location: winrt\imetadatatables.htm
tech.root: WinRT
ms.assetid: 30d06e87-93a2-4a9c-8843-4c42d7d9e3c8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMetaDataTables, IMetaDataTables interface [Windows Runtime], IMetaDataTables interface [Windows Runtime],described, rometadataapi/IMetaDataTables, winrt.imetadatatables
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataTables interface


## -description


Provides methods for the storage and retrieval of metadata information in tables.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataTables</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMetaDataTables</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1a9da245-a1a9-4004-8925-00b2fe72c9ca">GetBlob</a>
</td>
<td align="left" width="63%">
Gets a pointer to the binary large object (BLOB) at the specified column index.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9001b2ee-846e-476b-b1db-7860c25075ee">GetBlobHeapSize</a>
</td>
<td align="left" width="63%">
A pointer to a pointer to the binary data retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6467affc-0f86-4926-b72f-629c6580e1bf">GetCodedTokenInfo</a>
</td>
<td align="left" width="63%">
Gets a pointer to an array of tokens associated with the specified row index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69f80c79-5587-4740-b996-6c996e40ccf4">GetColumn</a>
</td>
<td align="left" width="63%">
Gets a pointer to the value contained in the cell of the specified column and row in the given table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aea7944a-87db-496c-869d-e9e2fa87e9af">GetColumnInfo</a>
</td>
<td align="left" width="63%">
Gets data about the specified column in the specified table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/037d722f-3efb-4c01-8445-b23caafbbdb2">GetGuid</a>
</td>
<td align="left" width="63%">
Gets a GUID from the row at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56b0f15f-caf3-44e0-8cec-7ca3f2edb74d">GetGuidHeapSize</a>
</td>
<td align="left" width="63%">
Gets the size, in bytes, of the GUID heap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f70e5377-4cc1-4066-acc2-bb13f336881b">GetNextBlob</a>
</td>
<td align="left" width="63%">
Gets the index of the next binary large object (BLOB) in the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b624f727-8371-49a1-8ec7-7110d9b8f971">GetNextGuid</a>
</td>
<td align="left" width="63%">
Gets the index of the next GUID value in the current table column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ac1fc2c-a60d-4431-8e49-5df1bb078c9b">GetNextString</a>
</td>
<td align="left" width="63%">
Gets the index of the next string in the current table column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d35a6622-df0a-4949-bc22-9bbd583337d4">GetNextUserString</a>
</td>
<td align="left" width="63%">
Gets the index of the row that contains the next hard-coded string in the current table column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5748a90-1ee1-4f76-93c0-2da2fd5d55c1">GetNumTables</a>
</td>
<td align="left" width="63%">
Gets the number of tables in the scope of the current IMetaDataTables instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d56bc0c8-0a63-48c8-bc2c-e3b4c2f313b8">GetRow</a>
</td>
<td align="left" width="63%">
Gets the row at the specified row index, in the table at the specified table index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35b79dac-39c7-4ca2-8608-e7ea64d4574c">GetString</a>
</td>
<td align="left" width="63%">
Gets the string at the specified index from the table column in the current reference scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c830b7c-2651-4efb-9d2d-989b5c25b72e">GetStringHeapSize</a>
</td>
<td align="left" width="63%">
Gets the size, in bytes, of the string heap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bc00076-f706-4941-84bd-f1b9c61934e5">GetTableIndex</a>
</td>
<td align="left" width="63%">
Gets the index for the table referenced by the specified token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2ba07df-4ccf-4563-b540-821008fc985c">GetTableInfo</a>
</td>
<td align="left" width="63%">
Gets the name, row size, number of rows, number of columns, and key column index of the specified table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/868f6be3-1baf-4f7c-be10-12b79a45e9c7">GetUserString</a>
</td>
<td align="left" width="63%">
Gets the hard-coded string at the specified index in the string column in the current scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f01059be-6370-4bab-b4f4-69db158c17a3">GetUserStringHeapSize</a>
</td>
<td align="left" width="63%">
Gets the size, in bytes, of the user string heap.

</td>
</tr>
</table> 

