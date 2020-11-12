---
UID: NF:cmdtree.ICommandTree.GetCommandTree
title: ICommandTree::GetCommandTree (cmdtree.h)
description: The ICommandTree::GetCommandTree method echoes the current command as a tree, including all post-processing operations that have been added.
helpviewer_keywords: ["GetCommandTree","GetCommandTree method [Indexing Service]","GetCommandTree method [Indexing Service]","ICommandTree interface","ICommandTree interface [Indexing Service]","GetCommandTree method","ICommandTree.GetCommandTree","ICommandTree::GetCommandTree","_idxs_ICommandTree_GetCommandTree","cmdtree/ICommandTree::GetCommandTree","indexsrv.icommandtree_getcommandtree"]
old-location: indexsrv\icommandtree_getcommandtree.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_2811.htm
ms.date: 12/05/2018
ms.keywords: GetCommandTree, GetCommandTree method [Indexing Service], GetCommandTree method [Indexing Service],ICommandTree interface, ICommandTree interface [Indexing Service],GetCommandTree method, ICommandTree.GetCommandTree, ICommandTree::GetCommandTree, _idxs_ICommandTree_GetCommandTree, cmdtree/ICommandTree::GetCommandTree, indexsrv.icommandtree_getcommandtree
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
 - ICommandTree::GetCommandTree
 - cmdtree/ICommandTree::GetCommandTree
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
 - ICommandTree.GetCommandTree
---

# ICommandTree::GetCommandTree


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>ICommandTree::GetCommandTree</b> method echoes the current command as a tree, including all post-processing operations that have been added.

## -parameters

### -param ppRoot [out]

The command object allocates memory for the command tree and returns the address to this memory; the consumer releases this memory with <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>, one node at a time, when it no longer needs the command tree. The provider sets <i>ppRoot</i> to a null pointer if an error occurs.

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
<dt><b>DB_S_ERRORSINTREE</b></dt>
</dl>
</td>
<td width="60%">
The provider discovered nonfatal errors in the command text previously set by <a href="/previous-versions/windows/desktop/ms709757(v=vs.85)">ICommandText::SetCommandText</a> while building the command tree.

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
The <i>ppRoot</i> parameter was a null pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The provider was unable to allocate sufficient memory in which to return the command tree.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DB_E_CANTTRANSLATE</b></dt>
</dl>
</td>
<td width="60%">
The provider cannot represent the command text previously set by <a href="/previous-versions/windows/desktop/ms709757(v=vs.85)">ICommandText::SetCommandText</a> as a tree.

</td>
</tr>
</table>

## -remarks

The returned tree reflects exactly the command set by the last invocation of <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-setcommandtree">ICommandTree::SetCommandTree</a> or <a href="/previous-versions/windows/desktop/ms709757(v=vs.85)">ICommandText::SetCommandText</a>, as modified by subsequent calls to <b>IQuery::AddPostProcessing</b>. If the command is stored as a tree, the returned tree is a copy of the one stored in the command object. If a tree node was passed with text, it is also echoed as text. If the command is stored as text, the provider should return a "navigable" command-tree representation of the text, which is not necessarily in optimized form. If the provider cannot create a full representation, the command tree can consist of a single text node. For example, if the tree can be represented as a DBOP_SQL_select node, and the provider supports that node, it must be returned in that format. However, if the tree cannot be represented as a DBOP_SQL_select node, but can be represented in a nontrivial command tree (that is, in a type other than DBOP_text_command), the provider must return it as that nontrivial tree. The provider may only return the tree as the trivial DBOP_text_command node, if that is the only command node it supports. Otherwise, it must return a valid, non-trivial navigable tree or return DB_E_CANTTRANSLATE if the text cannot be represented in such a tree. At this time, the provider should not make any unnecessary validation, such as binding, but if in the course of parsing the provider discovers nonfatal errors in building the tree, it should put the error information in the tree and return DB_S_ERRORSINTREE.

This method does not reveal a provider's internal, optimized translation (which may be different from a <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure) of text to (non-text) tree operations.

## -see-also

<a href="/previous-versions/windows/desktop/api/cmdtree/nn-cmdtree-icommandtree">ICommandTree</a>