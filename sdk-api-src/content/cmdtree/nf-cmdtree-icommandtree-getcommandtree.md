---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICommandTree::GetCommandTree


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>ICommandTree::GetCommandTree</b> method echoes the current command as a tree, including all post-processing operations that have been added.


## -parameters




### -param ppRoot [out]

The command object allocates memory for the command tree and returns the address to this memory; the consumer releases this memory with <a href="_com_imalloc_free">IMalloc::Free</a>, one node at a time, when it no longer needs the command tree. The provider sets <i>ppRoot</i> to a null pointer if an error occurs.


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
The provider discovered nonfatal errors in the command text previously set by <a href="0a077a8b-0673-4e81-ae2c-1f8d3191982c">ICommandText::SetCommandText</a> while building the command tree.

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
The provider cannot represent the command text previously set by <a href="0a077a8b-0673-4e81-ae2c-1f8d3191982c">ICommandText::SetCommandText</a> as a tree.

</td>
</tr>
</table>
 




## -remarks



The returned tree reflects exactly the command set by the last invocation of <a href="https://msdn.microsoft.com/13161978-498d-4a55-ba28-b15c66cf966f">ICommandTree::SetCommandTree</a> or <a href="0a077a8b-0673-4e81-ae2c-1f8d3191982c">ICommandText::SetCommandText</a>, as modified by subsequent calls to <b>IQuery::AddPostProcessing</b>. If the command is stored as a tree, the returned tree is a copy of the one stored in the command object. If a tree node was passed with text, it is also echoed as text. If the command is stored as text, the provider should return a "navigable" command-tree representation of the text, which is not necessarily in optimized form. If the provider cannot create a full representation, the command tree can consist of a single text node. For example, if the tree can be represented as a DBOP_SQL_select node, and the provider supports that node, it must be returned in that format. However, if the tree cannot be represented as a DBOP_SQL_select node, but can be represented in a nontrivial command tree (that is, in a type other than DBOP_text_command), the provider must return it as that nontrivial tree. The provider may only return the tree as the trivial DBOP_text_command node, if that is the only command node it supports. Otherwise, it must return a valid, non-trivial navigable tree or return DB_E_CANTTRANSLATE if the text cannot be represented in such a tree. At this time, the provider should not make any unnecessary validation, such as binding, but if in the course of parsing the provider discovers nonfatal errors in building the tree, it should put the error information in the tree and return DB_S_ERRORSINTREE.

This method does not reveal a provider's internal, optimized translation (which may be different from a <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure) of text to (non-text) tree operations.




## -see-also




<a href="https://msdn.microsoft.com/876a5c22-45bd-4b06-b323-532cd9230377">ICommandTree</a>
 

 

