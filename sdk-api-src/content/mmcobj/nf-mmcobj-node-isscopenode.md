---
UID: NF:mmcobj.Node.IsScopeNode
title: Node::IsScopeNode
author: windows-sdk-content
description: The IsScopeNode method returns whether the node is a scope node.
old-location: mmc\node_isscopenode.htm
old-project: mmc
ms.assetid: 1c01c520-b4c8-4109-92b4-2e1595259f3c
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: IsScopeNode, IsScopeNode method [MMC], IsScopeNode method [MMC],Node interface, IsScopeNode method [MMC],Node object, Node interface [MMC],IsScopeNode method, Node object [MMC],IsScopeNode method, Node.IsScopeNode, Node::IsScopeNode, _slate_node.isscopenode_method, mmc.node_isscopenode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MMCObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_PROPERTY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.exe
api_name:
 - Node.IsScopeNode
 - Node.IsScopeNode
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmc.exe
req.irql: 
req.product: GDI+ 1.1
---

# Node::IsScopeNode


## -description


The 
<b>IsScopeNode</b> method returns whether the node is a scope node.


## -parameters




### -param IsScopeNode






## -remarks



Nodes that appear in the scope tree are scope nodes. Be aware that the child of a scope node may also be a scope node. If the child of a scope node appears in both the scope tree and the result view, then calling the 
<b>IsScopeNode</b> method using the child's 
<a href="https://msdn.microsoft.com/c504cb3f-8ec6-49fe-b0d3-05ea9cad61f4">Node object</a> will return 1.


#### Examples

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Determine if the node is a scope node.
Dim lScopeNode As Long
lScopeNode = objNode.IsScopeNode()
If (1 = lScopeNode) Then
    MsgBox ("Node is a ScopeNode")
Else
    MsgBox ("Node is not a ScopeNode")
End If</pre>
</td>
</tr>
</table></span></div>


