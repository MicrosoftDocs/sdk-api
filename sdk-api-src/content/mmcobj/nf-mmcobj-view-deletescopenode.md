---
UID: NF:mmcobj.View.DeleteScopeNode
title: View::DeleteScopeNode
author: windows-sdk-content
description: The DeleteScopeNode method executes the Delete command for the specified node. If the context menu does not support Delete, then this method will not perform any operation.
old-location: mmc\view_deletescopenode.htm
old-project: mmc
ms.assetid: f7678d3a-4638-4b4d-8255-d9517217cd89
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: DeleteScopeNode, DeleteScopeNode method [MMC], DeleteScopeNode method [MMC],View interface, DeleteScopeNode method [MMC],View object, View interface [MMC],DeleteScopeNode method, View object [MMC],DeleteScopeNode method, View.DeleteScopeNode, View::DeleteScopeNode, _slate_view.deletescopenode_method, mmc.view_deletescopenode
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
 - View.DeleteScopeNode
 - View.DeleteScopeNode
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmc.exe
req.irql: 
req.product: GDI+ 1.1
---

# View::DeleteScopeNode


## -description


The 
<b>DeleteScopeNode</b> method executes the 
<b>Delete</b> command for the specified node. If the context menu does not support 
<b>Delete</b>, then this method will not perform any operation.


## -parameters




### -param ScopeNode

Optional. A value that specifies the node to be deleted; if this parameter is not specified, the active scope node is used.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/850516ae-4450-4773-8662-1e1bda805a30">View.DeleteSelection</a>
 

 

