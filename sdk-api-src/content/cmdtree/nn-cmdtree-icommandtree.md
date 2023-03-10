---
UID: NN:cmdtree.ICommandTree
title: ICommandTree (cmdtree.h)
description: The ICommandTree interface is optional for providers that support commands. It contains methods for manipulating query trees. Providers that support command trees must also support specifying the same functionality through the ICommandText interface.
helpviewer_keywords: ["ICommandTree","ICommandTree interface [Indexing Service]","ICommandTree interface [Indexing Service]","described","_idxs_ICommandTree","cmdtree/ICommandTree","indexsrv.icommandtree"]
old-location: indexsrv\icommandtree.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_0ckl.htm
ms.date: 12/05/2018
ms.keywords: ICommandTree, ICommandTree interface [Indexing Service], ICommandTree interface [Indexing Service],described, _idxs_ICommandTree, cmdtree/ICommandTree, indexsrv.icommandtree
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
 - ICommandTree
 - cmdtree/ICommandTree
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
 - ICommandTree
---

# ICommandTree interface


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>ICommandTree</b> interface is optional for providers that support commands. It contains methods for manipulating query trees. Providers that support command trees must also support specifying the same functionality through the <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommandText</a> interface.

A command object can have only one command; that command can be in the form of a command tree (specified in <b>ICommandTree</b>) or a text command (specified in <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommandText</a>). Thus, if a command is specified through the <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-setcommandtree">SetCommandTree</a> or <a href="/previous-versions/windows/desktop/ms709757(v=vs.85)">ICommandText::SetCommandText</a> methods, it replaces the command of the command object, whether that command was in text or tree form. If a command is retrieved through <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-getcommandtree">GetCommandTree</a> or <a href="/previous-versions/windows/desktop/ms709825(v=vs.85)">ICommandText::GetCommandText</a>, it is retrieved in the specified form, regardless of how the command was set. Thus, the <b>GetCommandText</b> method must be able to convert a command tree into command text, and the <b>GetCommandTree</b> method must be able to convert command text into a command tree. Note that in the latter conversion, the provider should return a navigable command tree representation of the text, which is not necessarily in optimized form. If the provider cannot create a full representation, the command tree can consist of a single text node.

Most providers will not permit an <b>ICommandTree</b> method to set a new command tree while there is a rowset open that was created by the command object. (The rowset directly reflects the result table of the original command tree). Some providers, however, may support this operation even while a rowset is open. If so, the output schema (set of columns) of the new command tree must include all columns for which there currently are accessors, and the accessors for all rowsets must remain valid. Open rowsets must be modified dynamically to reflect the result table of the new command tree. Return row handles (<i>hRows</i>) remain valid. This means that a new sort order or a new selection predicate are not effective for those rows, and that all accessors created after the command-tree modification will work with <i>hRows</i> obtained before the command-tree modification. If an error occurs while replacing or modifying a command tree with open rowsets, the command object, its command tree, the rowsets, <i>hRows</i>, and accessors remain unchanged.

## -inheritance

The <b>ICommandTree</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICommandTree</b> also has these types of members:

