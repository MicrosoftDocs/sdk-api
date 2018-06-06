---
UID: NF:ntquery.CIBuildQueryTree
title: CIBuildQueryTree function
author: windows-sdk-content
description: Builds a query restriction tree for a Command object.
old-location: indexsrv\cibuildquerytree.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_4b6t.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CIBuildQueryTree, CIBuildQueryTree function [Indexing Service], _idxs_CIBuildQueryTree, indexsrv.cibuildquerytree, ntquery/CIBuildQueryTree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MediaLabelInfo, *pMediaLabelInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntquery.dll
api_name:
 - CIBuildQueryTree
product: Windows
targetos: Windows
req.lib: Ntquery.lib
req.dll: Ntquery.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CIBuildQueryTree function


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Builds a query restriction tree for a Command object.


## -parameters




### -param pExistingTree

A pointer to a <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure representing the tree. This parameter can be <b>NULL</b>.


### -param dbBoolOp

The operation to be performed on the node. See <a href="https://msdn.microsoft.com/564e287b-ab3c-484e-8818-1d24ba5246ce">DBCOMMANDOP</a>.


### -param cSiblings

The number of sibling nodes for this node.


### -param ppSibsToCombine

A pointer to the address that contains the array of <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structures for the siblings to be combined with this node using the operation in <i>dbBoolOp</i>.


### -param ppTree

The address of the location to receive a pointer to the <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure for the tree structure.


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




<a href="https://msdn.microsoft.com/4efc1d6a-a646-4a88-8114-206a44531e41">CIBuildQueryNode</a>



<a href="https://msdn.microsoft.com/679b96f7-43b3-44c1-86dd-e995bb9a9c53">CITextToFullTree</a>



<a href="https://msdn.microsoft.com/095debd6-242f-4449-b5d7-1c2cae232bf4">CITextToFullTreeEx</a>



<a href="https://msdn.microsoft.com/333fb241-f484-4d79-89cd-9b1d8240b8a8">CITextToSelectTree</a>



<a href="https://msdn.microsoft.com/8d59e0f4-2c80-4d63-938b-91e7360c039b">CITextToSelectTreeEx</a>



<a href="https://msdn.microsoft.com/564e287b-ab3c-484e-8818-1d24ba5246ce">DBCOMMANDOP</a>



<a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a>
 

 

