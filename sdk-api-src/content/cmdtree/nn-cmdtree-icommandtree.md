---
UID: NN:cmdtree.ICommandTree
title: ICommandTree
author: windows-driver-content
description: The ICommandTree interface is optional for providers that support commands. It contains methods for manipulating query trees. Providers that support command trees must also support specifying the same functionality through the ICommandText interface.
old-location: indexsrv\icommandtree.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_0ckl.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ICommandTree, ICommandTree interface [Indexing Service], ICommandTree interface [Indexing Service],described, _idxs_ICommandTree, cmdtree/ICommandTree, indexsrv.icommandtree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	ICommandTree
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICommandTree interface


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>ICommandTree</b> interface is optional for providers that support commands. It contains methods for manipulating query trees. Providers that support command trees must also support specifying the same functionality through the <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommandText</a> interface.

A command object can have only one command; that command can be in the form of a command tree (specified in <b>ICommandTree</b>) or a text command (specified in <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommandText</a>). Thus, if a command is specified through the <a href="https://msdn.microsoft.com/13161978-498d-4a55-ba28-b15c66cf966f">SetCommandTree</a> or <a href="0a077a8b-0673-4e81-ae2c-1f8d3191982c">ICommandText::SetCommandText</a> methods, it replaces the command of the command object, whether that command was in text or tree form. If a command is retrieved through <a href="https://msdn.microsoft.com/e4f16873-45cd-444b-aab0-3ba3865b41a7">GetCommandTree</a> or <a href="0feeb66e-0a3b-418b-bf7e-b68ae8f4df13">ICommandText::GetCommandText</a>, it is retrieved in the specified form, regardless of how the command was set. Thus, the <b>GetCommandText</b> method must be able to convert a command tree into command text, and the <b>GetCommandTree</b> method must be able to convert command text into a command tree. Note that in the latter conversion, the provider should return a navigable command tree representation of the text, which is not necessarily in optimized form. If the provider cannot create a full representation, the command tree can consist of a single text node.

Most providers will not permit an <b>ICommandTree</b> method to set a new command tree while there is a rowset open that was created by the command object. (The rowset directly reflects the result table of the original command tree). Some providers, however, may support this operation even while a rowset is open. If so, the output schema (set of columns) of the new command tree must include all columns for which there currently are accessors, and the accessors for all rowsets must remain valid. Open rowsets must be modified dynamically to reflect the result table of the new command tree. Return row handles (<i>hRows</i>) remain valid. This means that a new sort order or a new selection predicate are not effective for those rows, and that all accessors created after the command-tree modification will work with <i>hRows</i> obtained before the command-tree modification. If an error occurs while replacing or modifying a command tree with open rowsets, the command object, its command tree, the rowsets, <i>hRows</i>, and accessors remain unchanged.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICommandTree</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICommandTree</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICommandTree</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55f6b6c9-9c22-46d2-a4b6-697501229046">FindErrorNodes</a>
</td>
<td align="left" width="63%">
Finds the error nodes on a tree. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d1de2d0-6851-46a1-98fb-5b188ee57a9b">FreeCommandTree</a>
</td>
<td align="left" width="63%">
Deallocates <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structures on a tree. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4f16873-45cd-444b-aab0-3ba3865b41a7">GetCommandTree</a>
</td>
<td align="left" width="63%">
Echoes a command as a command tree. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13161978-498d-4a55-ba28-b15c66cf966f">SetCommandTree</a>
</td>
<td align="left" width="63%">
Sets the command tree of a command object. 

</td>
</tr>
</table> 

