---
UID: NF:ntquery.CIBuildQueryNode
title: CIBuildQueryNode function (ntquery.h)
description: Builds one node of a query restriction tree for a Command object.
helpviewer_keywords: ["CIBuildQueryNode","CIBuildQueryNode function [Indexing Service]","_idxs_CIBuildQueryNode","indexsrv.cibuildquerynode","ntquery/CIBuildQueryNode"]
old-location: indexsrv\cibuildquerynode.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_0c11.htm
ms.date: 12/05/2018
ms.keywords: CIBuildQueryNode, CIBuildQueryNode function [Indexing Service], _idxs_CIBuildQueryNode, indexsrv.cibuildquerynode, ntquery/CIBuildQueryNode
f1_keywords:
- ntquery/CIBuildQueryNode
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
- CIBuildQueryNode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CIBuildQueryNode function


## -description


> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Builds one node of a query restriction tree for a Command object.


## -parameters




### -param wcsProperty

A pointer to a null-terminated string that specifies the friendly name for a property. The friendly name can be used in an Indexing Service query, column list, or sort order.


### -param dbOperator

The operation to be performed on the node. See <a href="/previous-versions/windows/desktop/indexsrv/dbcommandop">DBCOMMANDOP</a>.


### -param pvarPropertyValue

A pointer to the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure for the value to use for the <i>wcsProperty</i> parameter.


### -param ppTree

A pointer to an output variable that receives the pointer to the <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure for the node created by this function. 



### -param cProperties

The number of properties in the <i>pProperty</i> array.


### -param pProperty

A pointer to an array of <a href="/windows/desktop/api/ntquery/ns-ntquery-cipropertydef">CIPROPERTYDEF</a> structures, each of which describes a property that can be referred to by a friendly name. This array is populated when <i>pvarPropertyValue</i> contains a string that contains references to properties. This parameter can be <b>NULL</b> when <i>cProperties</i> equals zero.


### -param LocaleID

The locale ID used when converting properties. The <i>pvarPropertyValue</i> parameter itself contains a string that contains references to friendly property names, which are converted to uppercase for comparison and efficiency purposes.


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
<dt><b>QPARSE_E_NO_SUCH_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The function failed because the property name specified by <i>wcsProperty</i> was not found.

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
 




## -remarks



Use nodes created by the <b>CIBuildQueryNode</b> function to create or add to a query tree using the <a href="/windows/desktop/api/ntquery/nf-ntquery-cibuildquerytree">CIBuildQueryTree</a> function. Content properties are in turn passed to the <a href="/windows/desktop/api/ntquery/nf-ntquery-citexttoselecttree">CITextToSelectTree</a> function to create the <b>SELECT</b> part of the full tree.




## -see-also




<a href="/windows/desktop/api/ntquery/nf-ntquery-cibuildquerytree">CIBuildQueryTree</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-citexttofulltree">CITextToFullTree</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-citexttofulltreeex">CITextToFullTreeEx</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-citexttoselecttree">CITextToSelectTree</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-citexttoselecttreeex">CITextToSelectTreeEx</a>



<a href="/previous-versions/windows/desktop/indexsrv/dbcommandop">DBCOMMANDOP</a>



<a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a>
 

 