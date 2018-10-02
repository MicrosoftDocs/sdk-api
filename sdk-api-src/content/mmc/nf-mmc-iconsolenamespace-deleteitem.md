---
UID: NF:mmc.IConsoleNameSpace.DeleteItem
title: IConsoleNameSpace::DeleteItem
author: windows-sdk-content
description: Enables the snap-in to delete a single item from the scope pane.
old-location: mmc\iconsolenamespace_deleteitem.htm
tech.root: MMC
ms.assetid: 30455269-7E96-47D8-A4F7-E3F9AA6B251A
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DeleteItem, DeleteItem method [MMC], DeleteItem method [MMC],IConsoleNameSpace interface, IConsoleNameSpace interface [MMC],DeleteItem method, IConsoleNameSpace.DeleteItem, IConsoleNameSpace::DeleteItem, mmc.iconsolenamespace_deleteitem, mmc/IConsoleNameSpace::DeleteItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsoleNameSpace.DeleteItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleNameSpace::DeleteItem


## -description


Enables the snap-in to delete a single item from the scope pane.


## -parameters




### -param hItem [in]

A handle to the item whose child items are to be deleted from the scope pane. If the second argument to <b>IConsoleNameSpace::DeleteItem</b> is set to <b>TRUE</b>, the item is also deleted.


### -param fDeleteThis [in]

If <b>TRUE</b>, the item specified by hItem is also deleted; otherwise, it is not.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/444bc86d-bfd2-435c-b9fb-691c4da92411">IConsoleNameSpace</a>
 

 

