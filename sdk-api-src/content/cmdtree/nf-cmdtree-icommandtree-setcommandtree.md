---
UID: NF:cmdtree.ICommandTree.SetCommandTree
title: ICommandTree::SetCommandTree
author: windows-driver-content
description: The ICommandTree::SetCommandTree method sets a command object's command tree, replacing the existing one or replacing a text command specified with the ICommandText interface.
old-location: indexsrv\icommandtree_setcommandtree.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_6omd.htm
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: ICommandTree interface [Indexing Service],SetCommandTree method, ICommandTree.SetCommandTree, ICommandTree::SetCommandTree, SetCommandTree, SetCommandTree method [Indexing Service], SetCommandTree method [Indexing Service],ICommandTree interface, _idxs_ICommandTree_SetCommandTree, cmdtree/ICommandTree::SetCommandTree, indexsrv.icommandtree_setcommandtree
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SR_RESOURCE_TYPE_REPLICATED_PARTITION_INFO, *PSR_RESOURCE_TYPE_REPLICATED_PARTITION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	cmdtree.h
api_name:
-	ICommandTree.SetCommandTree
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICommandTree::SetCommandTree


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>ICommandTree::SetCommandTree</b> method sets a command object's command tree, replacing the existing one or replacing a text command specified with the <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommandText</a> interface. The provided command tree is copied into or transferred to, depending on the <i>fCopy</i> parameter, the command object. Thus, the consumer may delete the original tree or text without affecting the command object. Most error checking is deferred until one of the validation methods, optimization (see <a href="38e49e0c-5c87-43b9-ac8f-e901b4be23ad">ICommandPrepare</a>), or the <a href="95b4c895-a55c-4f01-a641-68a7f9a5f106">ICommand::Execute</a> method is invoked. This method only verifies that the command tree can indeed be copied into the command object's space.


## -parameters




### -param ppRoot [in]

Pointer to the address of the root of the command tree.


### -param dwCommandReuse [in]

A mask of type <a href="https://msdn.microsoft.com/0749eb01-c367-4290-a6c4-bbf0e1b97aec">DBCOMMANDREUSE</a> from the <a href="https://msdn.microsoft.com/09a29fb3-1daf-4074-899f-e32b3afd18f8">DBCOMMANDREUSEENUM</a> enumeration that specifies whether a state from the previous command is retained. If a state that was not previously specified is marked for reuse, the flag is ignored and no error occurs. Only DBCOMMANDREUSE_NONE is currently supported.


### -param fCopy [in]

If <b>TRUE</b>, the command tree is copied, and the caller retains ownership of the command tree's memory. If <b>FALSE</b>, the provider takes the entire tree, without copying, and sets the caller's root pointer to a <b>NULL</b> pointer. When the command object needs to deallocate the tree, it will call <a href="_com_imalloc_free">IMalloc::Free</a> once for each node in the tree.



If <i>fCopy</i> is <b>FALSE</b>, the consumer must not change the command tree without another call to the <b>SetCommandTree</b> method. The effect of any such change is undefined. In particular, the provider can assume that the command tree has not changed between the calls that use the tree, such as <b>SetCommandTree</b>, <a href="9c0302dd-0960-4f1b-8b74-4c3136b8e150">ICommandPrepare::Prepare</a>, and <a href="95b4c895-a55c-4f01-a641-68a7f9a5f106">ICommand::Execute</a>.


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
Either the <i>pRoot</i> parameter was a NULL pointer or the <i>dwCommandReuse</i> parameter was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DB_E_OBJECTOPEN</b></dt>
</dl>
</td>
<td width="60%">
A rowset was open on the command object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/876a5c22-45bd-4b06-b323-532cd9230377">ICommandTree</a>
 

 

