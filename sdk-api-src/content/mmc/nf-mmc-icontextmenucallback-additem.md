---
UID: NF:mmc.IContextMenuCallback.AddItem
title: IContextMenuCallback::AddItem
author: windows-sdk-content
description: The IContextMenuCallback::AddItem method adds a single item to a context menu.
old-location: mmc\icontextmenucallback_additem.htm
old-project: mmc
ms.assetid: 7186f201-13aa-4357-9b89-b435d244229c
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: AddItem, AddItem method [MMC], AddItem method [MMC],IContextMenuCallback interface, IContextMenuCallback interface [MMC],AddItem method, IContextMenuCallback.AddItem, IContextMenuCallback::AddItem, _slate_icontextmenucallback_additem, mmc.icontextmenucallback_additem, mmc/IContextMenuCallback::AddItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
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
 - IContextMenuCallback.AddItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IContextMenuCallback::AddItem


## -description


The <b>IContextMenuCallback::AddItem</b> method adds a single item to a context menu.


## -parameters




### -param pItem [in]

A pointer to a 
<a href="https://msdn.microsoft.com/58a0b4cf-0379-48a1-80c6-5245022cf891">CONTEXTMENUITEM</a> structure with the item to be added. This parameter cannot be <b>NULL</b>.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/58a0b4cf-0379-48a1-80c6-5245022cf891">CONTEXTMENUITEM</a>



<a href="https://msdn.microsoft.com/141a650f-a829-47b1-abf9-427302d98444">IContextMenuCallback</a>
 

 

