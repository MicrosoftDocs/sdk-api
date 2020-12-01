---
UID: NF:cmdtree.ICommandTree.FindErrorNodes
title: ICommandTree::FindErrorNodes (cmdtree.h)
description: The ICommandTree::FindErrorNodes method traverses a command tree and returns an array of nodes with errors in them.
helpviewer_keywords: ["FindErrorNodes","FindErrorNodes method [Indexing Service]","FindErrorNodes method [Indexing Service]","ICommandTree interface","ICommandTree interface [Indexing Service]","FindErrorNodes method","ICommandTree.FindErrorNodes","ICommandTree::FindErrorNodes","_idxs_ICommandTree_FindErrorNodes","cmdtree/ICommandTree::FindErrorNodes","indexsrv.icommandtree_finderrornodes"]
old-location: indexsrv\icommandtree_finderrornodes.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_68tv.htm
ms.date: 12/05/2018
ms.keywords: FindErrorNodes, FindErrorNodes method [Indexing Service], FindErrorNodes method [Indexing Service],ICommandTree interface, ICommandTree interface [Indexing Service],FindErrorNodes method, ICommandTree.FindErrorNodes, ICommandTree::FindErrorNodes, _idxs_ICommandTree_FindErrorNodes, cmdtree/ICommandTree::FindErrorNodes, indexsrv.icommandtree_finderrornodes
req.header: cmdtree.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CmdTre.idl
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
 - ICommandTree::FindErrorNodes
 - cmdtree/ICommandTree::FindErrorNodes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cmdtree.h
api_name:
 - ICommandTree.FindErrorNodes
---

# ICommandTree::FindErrorNodes


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>ICommandTree::FindErrorNodes</b> method traverses a command tree and returns an array of nodes with errors in them.

## -parameters

### -param pRoot [in]

A pointer to the root of the command tree.

### -param pcErrorNodes [out]

A pointer to memory in which to return the number of nodes containing errors.

### -param prgErrorNodes [out]

A pointer to memory in which to return an array of pointers to nodes that contain errors. The command object allocates memory for this array and returns the address to this memory; the consumer releases this memory with <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a> when it no longer needs the array. If *<i>pcErrorNodes</i> is 0 on output, the provider does not allocate any memory and thus ensures that *<i>prgErrorNodes</i> is a null pointer on output.

## -returns

This method can return one of these values.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
A provider-specific error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pRoots</i>, <i>pcErrorNodes</i>, or <i>prgErrorNodes</i> was a null pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The provider was unable to allocate sufficient memory in which to return the array of pointers to nodes containing errors.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/cmdtree/nn-cmdtree-icommandtree">ICommandTree</a>