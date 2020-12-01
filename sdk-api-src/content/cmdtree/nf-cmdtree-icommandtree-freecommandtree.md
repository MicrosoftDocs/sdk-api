---
UID: NF:cmdtree.ICommandTree.FreeCommandTree
title: ICommandTree::FreeCommandTree (cmdtree.h)
description: The ICommandTree::FreeCommandTree method traverses a command tree and deallocates all DBCOMMANDTREE node structures, as well as all variants in those structures. It then sets the root pointer to a NULL pointer.
helpviewer_keywords: ["FreeCommandTree","FreeCommandTree method [Indexing Service]","FreeCommandTree method [Indexing Service]","ICommandTree interface","ICommandTree interface [Indexing Service]","FreeCommandTree method","ICommandTree.FreeCommandTree","ICommandTree::FreeCommandTree","_idxs_ICommandTree_FreeCommandTree","cmdtree/ICommandTree::FreeCommandTree","indexsrv.icommandtree_freecommandtree"]
old-location: indexsrv\icommandtree_freecommandtree.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_1v39.htm
ms.date: 12/05/2018
ms.keywords: FreeCommandTree, FreeCommandTree method [Indexing Service], FreeCommandTree method [Indexing Service],ICommandTree interface, ICommandTree interface [Indexing Service],FreeCommandTree method, ICommandTree.FreeCommandTree, ICommandTree::FreeCommandTree, _idxs_ICommandTree_FreeCommandTree, cmdtree/ICommandTree::FreeCommandTree, indexsrv.icommandtree_freecommandtree
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
 - ICommandTree::FreeCommandTree
 - cmdtree/ICommandTree::FreeCommandTree
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
 - ICommandTree.FreeCommandTree
---

# ICommandTree::FreeCommandTree


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>ICommandTree::FreeCommandTree</b> method traverses a command tree and deallocates all <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> node structures, as well as all variants in those structures. It then sets the root pointer to a <b>NULL</b> pointer.

## -parameters

### -param ppRoot [in]

Pointer to a variable that receives the pointer to the root of the command tree on successful exit.

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
The <i>ppRoot</i> parameter was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DB_E_CANNOTFREE</b></dt>
</dl>
</td>
<td width="60%">
The consumer called the <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-setcommandtree">ICommandTree::SetCommandTree</a> method with <i>fCopy</i> = <b>FALSE</b>, thereby relinquishing ownership of the memory to the provider.

</td>
</tr>
</table>

## -remarks

The <b>FreeCommandTree</b> method can be used by a consumer to free its copy of the command tree constructed locally or obtained by <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-getcommandtree">ICommandTree::GetCommandTree</a>. It does not free the copy of the tree owned by the command object. When a consumer calls <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-setcommandtree">SetCommandTree</a> with <i>fCopy</i> = <b>FALSE</b>, the consumer relinquishes ownership of the memory to the provider. Therefore, if the consumer calls <b>FreeCommandTree</b> after having called <b>SetCommandTree</b> with <i>fCopy</i> = <b>FALSE</b>, <b>FreeCommandTree</b> returns a DB_E_CANNOTFREE error code, meaning the consumer does not have ownership of the tree and is unable to free it.

## -see-also

<a href="/previous-versions/windows/desktop/api/cmdtree/nn-cmdtree-icommandtree">ICommandTree</a>