---
UID: NF:mmc.IConsoleNameSpace.DeleteItem
title: IConsoleNameSpace::DeleteItem
author: windows-sdk-content
description: The IConsoleNameSpace2::DeleteItem method enables the snap-in to delete a single item from the scope pane.
old-location: mmc\iconsolenamespace2_deleteitem.htm
old-project: mmc
ms.assetid: 488a6c26-e064-44a1-9842-6f41ec25887c
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: DeleteItem, DeleteItem method [MMC], DeleteItem method [MMC],IConsoleNameSpace interface, DeleteItem method [MMC],IConsoleNameSpace2 interface, IConsoleNameSpace interface [MMC],DeleteItem method, IConsoleNameSpace.DeleteItem, IConsoleNameSpace2 interface [MMC],DeleteItem method, IConsoleNameSpace2::DeleteItem, IConsoleNameSpace::DeleteItem, _slate_iconsolenamespace2_deleteitem, mmc.iconsolenamespace2_deleteitem, mmc/IConsoleNameSpace2::DeleteItem, mmc/IConsoleNameSpace::DeleteItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsoleNameSpace.DeleteItem
 - IConsoleNameSpace2.DeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsoleNameSpace::DeleteItem


## -description


The <b>IConsoleNameSpace2::DeleteItem</b> method enables the snap-in to delete a single item from the scope pane.


## -parameters




### -param hItem [in]

A handle to the item whose child items are to be deleted from the scope pane. If the second argument to <b>IConsoleNameSpace2::DeleteItem</b> is set to <b>TRUE</b>, the item is also deleted.


### -param fDeleteThis [in]

If <b>TRUE</b>, the item specified by hItem is also deleted; otherwise, it is not.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/894f99a6-2189-458d-a50f-497930d4a9dd">IConsoleNameSpace2</a>
 

 

