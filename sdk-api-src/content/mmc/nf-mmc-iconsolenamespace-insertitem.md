---
UID: NF:mmc.IConsoleNameSpace.InsertItem
title: IConsoleNameSpace::InsertItem
author: windows-sdk-content
description: The IConsoleNameSpace2::InsertItem method enables the snap-in to insert a single item into the scope view.
old-location: mmc\iconsolenamespace2_insertitem.htm
tech.root: mmc
ms.assetid: 1966c4d1-acb1-496a-92d2-c0437c95fba6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IConsoleNameSpace interface [MMC],InsertItem method, IConsoleNameSpace.InsertItem, IConsoleNameSpace2 interface [MMC],InsertItem method, IConsoleNameSpace2::InsertItem, IConsoleNameSpace::InsertItem, InsertItem, InsertItem method [MMC], InsertItem method [MMC],IConsoleNameSpace interface, InsertItem method [MMC],IConsoleNameSpace2 interface, _slate_iconsolenamespace2_insertitem, mmc.iconsolenamespace2_insertitem, mmc/IConsoleNameSpace2::InsertItem, mmc/IConsoleNameSpace::InsertItem
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
 - IConsoleNameSpace.InsertItem
 - IConsoleNameSpace2.InsertItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleNameSpace::InsertItem


## -description


The <b>IConsoleNameSpace2::InsertItem</b> method enables the snap-in to insert a single item into the scope view.


## -parameters




### -param item [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c392f25c-80e7-4c91-9063-36143320b9aa">SCOPEDATAITEM</a> structure that specifies the attributes of the new scope item. On return, the 
ID member of the structure contains the item identifier assigned by MMC for the newly inserted item. Be aware that this value is the <b>HSCOPEITEM</b> handle of the inserted item. The snap-in should store this value in order to later manipulate the inserted item by calling methods such as 
<a href="https://msdn.microsoft.com/0dadf9f0-4d49-49c3-a190-dfab0d6ace3f">IConsoleNameSpace2::GetItem</a>.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt300831(v=VS.85).aspx">IConsoleNameSpace</a>



<a href="https://msdn.microsoft.com/894f99a6-2189-458d-a50f-497930d4a9dd">IConsoleNameSpace2</a>
 

 

