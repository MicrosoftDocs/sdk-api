---
UID: NF:ntquery.CIBuildQueryTree
title: CIBuildQueryTree function (ntquery.h)
description: Builds a query restriction tree for a Command object.
helpviewer_keywords: ["CIBuildQueryTree","CIBuildQueryTree function [Indexing Service]","_idxs_CIBuildQueryTree","indexsrv.cibuildquerytree","ntquery/CIBuildQueryTree"]
old-location: indexsrv\cibuildquerytree.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_4b6t.htm
ms.date: 12/05/2018
ms.keywords: CIBuildQueryTree, CIBuildQueryTree function [Indexing Service], _idxs_CIBuildQueryTree, indexsrv.cibuildquerytree, ntquery/CIBuildQueryTree
f1_keywords:
- ntquery/CIBuildQueryTree
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
- CIBuildQueryTree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CIBuildQueryTree function


## -description


> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Builds a query restriction tree for a Command object.


## -parameters




### -param pExistingTree

A pointer to a <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure representing the tree. This parameter can be <b>NULL</b>.


### -param dbBoolOp

The operation to be performed on the node. See <a href="/previous-versions/windows/desktop/indexsrv/dbcommandop">DBCOMMANDOP</a>.


### -param cSiblings

The number of sibling nodes for this node.


### -param ppSibsToCombine

A pointer to the address that contains the array of <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structures for the siblings to be combined with this node using the operation in <i>dbBoolOp</i>.


### -param ppTree

The address of the location to receive a pointer to the <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure for the tree structure.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The function was denied access to the specified path.

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
The number of operands (siblings) for the specified <i>dbBoolOp</i> is not correct.

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




<a href="/windows/desktop/api/ntquery/nf-ntquery-cibuildquerynode">CIBuildQueryNode</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-citexttofulltree">CITextToFullTree</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-citexttofulltreeex">CITextToFullTreeEx</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-citexttoselecttree">CITextToSelectTree</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-citexttoselecttreeex">CITextToSelectTreeEx</a>



<a href="/previous-versions/windows/desktop/indexsrv/dbcommandop">DBCOMMANDOP</a>



<a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a>
 

 