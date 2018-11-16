---
UID: NF:mmc.IContextMenuCallback2.AddItem
title: IContextMenuCallback2::AddItem
author: windows-sdk-content
description: The IContextMenuCallback2::AddItem method adds a single item to a context menu.
old-location: mmc\icontextmenucallback2_additem.htm
tech.root: MMC
ms.assetid: 11a43bf5-dce0-4bcb-b003-95c31d9fd171
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddItem, AddItem method [MMC], AddItem method [MMC],IContextMenuCallback2 interface, IContextMenuCallback2 interface [MMC],AddItem method, IContextMenuCallback2.AddItem, IContextMenuCallback2::AddItem, _slate_icontextmenucallback2_additem, mmc.icontextmenucallback2_additem, mmc/IContextMenuCallback2::AddItem
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
req.lib: Mmc.lib
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
 - IContextMenuCallback2.AddItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmc.h
: 
- IContextMenuCallback2.AddItem
: 
---

# IContextMenuCallback2::AddItem


## -description


The <b>IContextMenuCallback2::AddItem</b> method adds a single item to a context menu.


## -parameters




### -param pItem [in]

A pointer to a 
<a href="https://msdn.microsoft.com/5ed4429c-e147-4097-8d52-11f5319dce2a">CONTEXTMENUITEM2</a> structure with the item to be added. This parameter cannot be <b>NULL</b>.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/5ed4429c-e147-4097-8d52-11f5319dce2a">CONTEXTMENUITEM2</a>



<a href="https://msdn.microsoft.com/97f0f574-6575-4be6-9c30-ed68e3438d30">IContextMenuCallback2</a>
 

 

