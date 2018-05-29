---
UID: NF:cmdtree.ICommandTree.FindErrorNodes
title: ICommandTree::FindErrorNodes
author: windows-sdk-content
description: The ICommandTree::FindErrorNodes method traverses a command tree and returns an array of nodes with errors in them.
old-location: indexsrv\icommandtree_finderrornodes.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_68tv.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: FindErrorNodes, FindErrorNodes method [Indexing Service], FindErrorNodes method [Indexing Service],ICommandTree interface, ICommandTree interface [Indexing Service],FindErrorNodes method, ICommandTree.FindErrorNodes, ICommandTree::FindErrorNodes, _idxs_ICommandTree_FindErrorNodes, cmdtree/ICommandTree::FindErrorNodes, indexsrv.icommandtree_finderrornodes
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	cmdtree.h
api_name:
-	ICommandTree.FindErrorNodes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICommandTree::FindErrorNodes


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>ICommandTree::FindErrorNodes</b> method traverses a command tree and returns an array of nodes with errors in them.


## -parameters




### -param pRoot [in]

A pointer to the root of the command tree.


### -param pcErrorNodes [out]

A pointer to memory in which to return the number of nodes containing errors.


### -param prgErrorNodes [out]

A pointer to memory in which to return an array of pointers to nodes that contain errors. The command object allocates memory for this array and returns the address to this memory; the consumer releases this memory with <a href="_com_imalloc_free">IMalloc::Free</a> when it no longer needs the array. If *<i>pcErrorNodes</i> is 0 on output, the provider does not allocate any memory and thus ensures that *<i>prgErrorNodes</i> is a null pointer on output.


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




<a href="https://msdn.microsoft.com/876a5c22-45bd-4b06-b323-532cd9230377">ICommandTree</a>
 

 

