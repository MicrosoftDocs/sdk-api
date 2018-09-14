---
UID: NF:mmc.IConsoleNameSpace.InsertItem
title: IConsoleNameSpace::InsertItem
author: windows-sdk-content
description: Enables the snap-in to insert a single item into the scope view.
old-location: mmc\iconsolenamespace_insertitem.htm
tech.root: mmc
ms.assetid: E496C159-0FCE-490B-995B-2841517BEACB
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: IConsoleNameSpace interface [MMC],InsertItem method, IConsoleNameSpace.InsertItem, IConsoleNameSpace::InsertItem, InsertItem, InsertItem method [MMC], InsertItem method [MMC],IConsoleNameSpace interface, mmc.iconsolenamespace_insertitem, mmc/IConsoleNameSpace::InsertItem
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
 - IConsoleNameSpace.InsertItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleNameSpace::InsertItem


## -description


Enables the snap-in to insert a single item into the scope view.


## -parameters




### -param item [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c392f25c-80e7-4c91-9063-36143320b9aa">SCOPEDATAITEM</a> structure that specifies the attributes of the new scope item. On return, the 
ID member of the structure contains the item identifier assigned by MMC for the newly inserted item. Be aware that this value is the <b>HSCOPEITEM</b> handle of the inserted item. The snap-in should store this value in order to later manipulate the inserted item by calling methods such as 
<a href="https://msdn.microsoft.com/72c4cafb-f39b-4e37-b8f0-4f0867ac78f0">IConsoleNameSpace::GetItem</a>.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/444bc86d-bfd2-435c-b9fb-691c4da92411">IConsoleNameSpace</a>
 

 

