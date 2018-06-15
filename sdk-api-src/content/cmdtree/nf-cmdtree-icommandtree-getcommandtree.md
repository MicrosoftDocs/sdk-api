---
UID: NF:cmdtree.ICommandTree.GetCommandTree
title: ICommandTree::GetCommandTree
author: windows-sdk-content
description: The ICommandTree::GetCommandTree method echoes the current command as a tree, including all post-processing operations that have been added.
old-location: indexsrv\icommandtree_getcommandtree.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_2811.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetCommandTree, GetCommandTree method [Indexing Service], GetCommandTree method [Indexing Service],ICommandTree interface, ICommandTree interface [Indexing Service],GetCommandTree method, ICommandTree.GetCommandTree, ICommandTree::GetCommandTree, _idxs_ICommandTree_GetCommandTree, cmdtree/ICommandTree::GetCommandTree, indexsrv.icommandtree_getcommandtree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cmdtree.h
api_name:
 - ICommandTree.GetCommandTree
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICommandTree::GetCommandTree


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

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
The provider discovered nonfatal errors in the command text previously set by <a href="https://msdn.microsoft.com/library/windows/desktop/0a077a8b-0673-4e81-ae2c-1f8d3191982c">ICommandText::SetCommandText</a> while building the command tree.

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
The provider cannot represent the command text previously set by <a href="https://msdn.microsoft.com/library/windows/desktop/0a077a8b-0673-4e81-ae2c-1f8d3191982c">ICommandText::SetCommandText</a> as a tree.

</td>
</tr>
</table>
 




## -remarks



The returned tree reflects exactly the command set by the last invocation of <a href="https://msdn.microsoft.com/13161978-498d-4a55-ba28-b15c66cf966f">ICommandTree::SetCommandTree</a> or <a href="https://msdn.microsoft.com/library/windows/desktop/0a077a8b-0673-4e81-ae2c-1f8d3191982c">ICommandText::SetCommandText</a>, as modified by subsequent calls to <b>IQuery::AddPostProcessing</b>. If the command is stored as a tree, the returned tree is a copy of the one stored in the command object. If a tree node was passed with text, it is also echoed as text. If the command is stored as text, the provider should return a "navigable" command-tree representation of the text, which is not necessarily in optimized form. If the provider cannot create a full representation, the command tree can consist of a single text node. For example, if the tree can be represented as a DBOP_SQL_select node, and the provider supports that node, it must be returned in that format. However, if the tree cannot be represented as a DBOP_SQL_select node, but can be represented in a nontrivial command tree (that is, in a type other than DBOP_text_command), the provider must return it as that nontrivial tree. The provider may only return the tree as the trivial DBOP_text_command node, if that is the only command node it supports. Otherwise, it must return a valid, non-trivial navigable tree or return DB_E_CANTTRANSLATE if the text cannot be represented in such a tree. At this time, the provider should not make any unnecessary validation, such as binding, but if in the course of parsing the provider discovers nonfatal errors in building the tree, it should put the error information in the tree and return DB_S_ERRORSINTREE.

This method does not reveal a provider's internal, optimized translation (which may be different from a <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure) of text to (non-text) tree operations.




## -see-also




<a href="https://msdn.microsoft.com/876a5c22-45bd-4b06-b323-532cd9230377">ICommandTree</a>
 

 

