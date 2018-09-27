---
UID: NF:mmc.IConsoleNameSpace2.Expand
title: IConsoleNameSpace2::Expand
author: windows-sdk-content
description: The IConsoleNameSpace2::Expand method enables the snap-in to expand an item in the namespace without visibly expanding the item in the scope pane.
old-location: mmc\iconsolenamespace2_expand.htm
tech.root: mmc
ms.assetid: 3672babb-b172-4f25-8d95-61f3aacce2f0
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: Expand, Expand method [MMC], Expand method [MMC],IConsoleNameSpace2 interface, IConsoleNameSpace2 interface [MMC],Expand method, IConsoleNameSpace2.Expand, IConsoleNameSpace2::Expand, _slate_iconsolenamespace2_expand, mmc.iconsolenamespace2_expand, mmc/IConsoleNameSpace2::Expand
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
req.idl: 
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
 - IConsoleNameSpace2.Expand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleNameSpace2::Expand


## -description


The <b>IConsoleNameSpace2::Expand</b> method enables the snap-in to expand an item in the namespace without visibly expanding the item in the scope pane.


## -parameters




### -param hItem [in]

A handle to the item to expand.


## -returns



This method can return one of these values.




## -remarks



<b>IConsoleNameSpace2::Expand</b> should be used to expand a specified item for the purpose of enumerating the child items of that item. Be aware that you must call <b>IConsoleNameSpace2::Expand</b> before inserting an item as a child item in the scope pane.

For example, if a snap-in must place a child item beneath a parent item at a specific position (such as the top of a child item list), the snap-in should use this method to expand the item to find the exact position in which to place a child item. The snap-in could also use this method to call 
<a href="https://msdn.microsoft.com/a320f42e-1dca-4dd9-a919-c4451a48d105">IConsoleNameSpace2::GetChildItem</a> on a child item of an item that has not been expanded (either by a previous call to <b>IConsoleNameSpace2::Expand</b> or by the user clicking the plus sign in the scope pane) to expand that item for the purpose of enumerating its children.

<b>IConsoleNameSpace2::Expand</b> does not visibly expand the item in the tree displayed in the scope pane in the console. A snap-in uses 
<a href="https://msdn.microsoft.com/958c9611-fd9c-4895-903b-145eacf76901">IConsole2::Expand</a> to visibly expand or collapse an item in the scope pane. This method sends an <a href="https://msdn.microsoft.com/de89a195-082b-4d5f-bd8c-1c75215ab60f">MMCN_EXPAND</a> notification to 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> if and only if the item has not been previously expanded.




## -see-also




<a href="https://msdn.microsoft.com/894f99a6-2189-458d-a50f-497930d4a9dd">IConsoleNameSpace2</a>
 

 

