---
UID: NF:mmc.IConsoleNameSpace.GetItem
title: IConsoleNameSpace::GetItem
author: windows-sdk-content
description: The IConsoleNameSpace2::GetItem method enables the snap-in to retrieve some or all of a single scope item's attributes.
old-location: mmc\iconsolenamespace2_getitem.htm
old-project: MMC
ms.assetid: 0dadf9f0-4d49-49c3-a190-dfab0d6ace3f
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetItem, GetItem method [MMC], GetItem method [MMC],IConsoleNameSpace interface, GetItem method [MMC],IConsoleNameSpace2 interface, IConsoleNameSpace interface [MMC],GetItem method, IConsoleNameSpace.GetItem, IConsoleNameSpace2 interface [MMC],GetItem method, IConsoleNameSpace2::GetItem, IConsoleNameSpace::GetItem, _slate_iconsolenamespace2_getitem, mmc.iconsolenamespace2_getitem, mmc/IConsoleNameSpace2::GetItem, mmc/IConsoleNameSpace::GetItem
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
 - IConsoleNameSpace.GetItem
 - IConsoleNameSpace2.GetItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsoleNameSpace::GetItem


## -description


The <b>IConsoleNameSpace2::GetItem</b> method enables the snap-in to retrieve some or all of a single scope item's attributes.


## -parameters




### -param item [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c392f25c-80e7-4c91-9063-36143320b9aa">SCOPEDATAITEM</a> structure that specifies the information to retrieve and receives information about the item. When the message is sent, the 
ID member of the structure identifies the item and the mask member specifies the attributes to retrieve.

If mask specifies the <b>SDI_STATE</b> value, the <b>nState</b> member contains the item's state information.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/894f99a6-2189-458d-a50f-497930d4a9dd">IConsoleNameSpace2</a>
 

 

