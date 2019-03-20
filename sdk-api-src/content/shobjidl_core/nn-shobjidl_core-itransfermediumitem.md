---
UID: NN:shobjidl_core.ITransferMediumItem
title: ITransferMediumItem (shobjidl_core.h)
author: windows-sdk-content
description: Used by a copy engine to get the item on which to call QueryInterface to return a pointer to interface ITransferDestination or interface ITransferSource. These interfaces can be queried and enumerated for copy, move, or delete operations.
old-location: shell\ITransferMediumItem.htm
tech.root: shell
ms.assetid: 28b4397c-dcb1-4c81-b6a3-d6abd7f7ad24
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITransferMediumItem, ITransferMediumItem interface [Windows Shell], ITransferMediumItem interface [Windows Shell],described, _shell_ITransferMediumItem, shell.ITransferMediumItem, shobjidl_core/ITransferMediumItem
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ITransferMediumItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransferMediumItem interface


## -description


Used by a copy engine to get the item on which to call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to return a pointer to interface <a href="https://msdn.microsoft.com/8d0049e0-e227-40ae-a282-cdc17f227e24">ITransferDestination</a> or interface <a href="https://msdn.microsoft.com/341966d4-f9cf-457d-97ef-8e6107544283">ITransferSource</a>. These interfaces can be queried and enumerated for copy, move, or delete operations.


## -remarks



This interface provides only the methods of the <a href="https://msdn.microsoft.com/f42d218c-0251-45e0-b05a-f1ccdcaf036c">IRelatedItem</a> interface, from which it inherits.



