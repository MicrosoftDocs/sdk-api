---
UID: NF:cmdtree.ICommandTree.SetCommandTree
title: ICommandTree::SetCommandTree (cmdtree.h)
description: The ICommandTree::SetCommandTree method sets a command object's command tree, replacing the existing one or replacing a text command specified with the ICommandText interface.
helpviewer_keywords: ["ICommandTree interface [Indexing Service]","SetCommandTree method","ICommandTree.SetCommandTree","ICommandTree::SetCommandTree","SetCommandTree","SetCommandTree method [Indexing Service]","SetCommandTree method [Indexing Service]","ICommandTree interface","_idxs_ICommandTree_SetCommandTree","cmdtree/ICommandTree::SetCommandTree","indexsrv.icommandtree_setcommandtree"]
old-location: indexsrv\icommandtree_setcommandtree.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_6omd.htm
ms.date: 12/05/2018
ms.keywords: ICommandTree interface [Indexing Service],SetCommandTree method, ICommandTree.SetCommandTree, ICommandTree::SetCommandTree, SetCommandTree, SetCommandTree method [Indexing Service], SetCommandTree method [Indexing Service],ICommandTree interface, _idxs_ICommandTree_SetCommandTree, cmdtree/ICommandTree::SetCommandTree, indexsrv.icommandtree_setcommandtree
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
 - ICommandTree::SetCommandTree
 - cmdtree/ICommandTree::SetCommandTree
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
 - ICommandTree.SetCommandTree
---

# ICommandTree::SetCommandTree


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>ICommandTree::SetCommandTree</b> method sets a command object's command tree, replacing the existing one or replacing a text command specified with the <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommandText</a> interface. The provided command tree is copied into or transferred to, depending on the <i>fCopy</i> parameter, the command object. Thus, the consumer may delete the original tree or text without affecting the command object. Most error checking is deferred until one of the validation methods, optimization (see <a href="/previous-versions/windows/desktop/ms713621(v=vs.85)">ICommandPrepare</a>), or the <a href="/previous-versions/windows/desktop/ms718095(v=vs.85)">ICommand::Execute</a> method is invoked. This method only verifies that the command tree can indeed be copied into the command object's space.

## -parameters

### -param ppRoot [in]

Pointer to the address of the root of the command tree.

### -param dwCommandReuse [in]

A mask of type <a href="/previous-versions/windows/desktop/indexsrv/dbcommandreuse">DBCOMMANDREUSE</a> from the <a href="/previous-versions/windows/desktop/api/cmdtree/ne-cmdtree-dbcommandreuseenum">DBCOMMANDREUSEENUM</a> enumeration that specifies whether a state from the previous command is retained. If a state that was not previously specified is marked for reuse, the flag is ignored and no error occurs. Only DBCOMMANDREUSE_NONE is currently supported.

### -param fCopy [in]

If <b>TRUE</b>, the command tree is copied, and the caller retains ownership of the command tree's memory. If <b>FALSE</b>, the provider takes the entire tree, without copying, and sets the caller's root pointer to a <b>NULL</b> pointer. When the command object needs to deallocate the tree, it will call <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a> once for each node in the tree.



If <i>fCopy</i> is <b>FALSE</b>, the consumer must not change the command tree without another call to the <b>SetCommandTree</b> method. The effect of any such change is undefined. In particular, the provider can assume that the command tree has not changed between the calls that use the tree, such as <b>SetCommandTree</b>, <a href="/previous-versions/windows/desktop/ms718370(v=vs.85)">ICommandPrepare::Prepare</a>, and <a href="/previous-versions/windows/desktop/ms718095(v=vs.85)">ICommand::Execute</a>.

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

<a href="/previous-versions/windows/desktop/api/cmdtree/nn-cmdtree-icommandtree">ICommandTree</a>