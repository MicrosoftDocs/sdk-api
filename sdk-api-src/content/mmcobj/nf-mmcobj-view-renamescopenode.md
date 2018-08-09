---
UID: NF:mmcobj.View.RenameScopeNode
title: View::RenameScopeNode
author: windows-sdk-content
description: The RenameScopeNode method renames a node.
old-location: mmc\view_renamescopenode.htm
old-project: MMC
ms.assetid: b5034924-fa90-41ec-8d02-02a2c294eae9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: RenameScopeNode, RenameScopeNode method [MMC], RenameScopeNode method [MMC],View interface, RenameScopeNode method [MMC],View object, View interface [MMC],RenameScopeNode method, View object [MMC],RenameScopeNode method, View.RenameScopeNode, View::RenameScopeNode, _slate_view.renamescopenode_method, mmc.view_renamescopenode
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
 - View.RenameScopeNode
 - View.RenameScopeNode
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmc.exe
req.irql: 
req.product: GDI+ 1.1
---

# View::RenameScopeNode


## -description


The 
<b>RenameScopeNode</b> method renames a node.


## -parameters




### -param NewName

The new name for the node.


### -param ScopeNode

Optional. A value that specifies the node to be renamed; if this parameter is not specified, the active scope node is used.


## -returns



This method does not return a value.




## -remarks



Attempting to change a node name that cannot be changed results in a Windows Script Host error.


#### Examples

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' This example renames the Document object's RootNode.
' Retrieve the RootNode object.
Dim var1 As Variant
Set var1 = objDoc.RootNode
 
' Rename the scope node.
objView.RenameScopeNode "New Console Root", var1
 
' Free the Variant when done.
Set var1 = Nothing</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/65788a9f-7d56-4114-8cb7-479f3899d418">View.RenameSelectedItem</a>
 

 

