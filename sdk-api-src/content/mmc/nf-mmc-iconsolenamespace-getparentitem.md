---
UID: NF:mmc.IConsoleNameSpace.GetParentItem
title: IConsoleNameSpace::GetParentItem
author: windows-sdk-content
description: Enables the snap-in to retrieve the handle to a parent item in the scope view.
old-location: mmc\iconsolenamespace_getparentitem.htm
tech.root: MMC
ms.assetid: 6F053540-D14D-4E5A-891C-00B140A5DFBC
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetParentItem, GetParentItem method [MMC], GetParentItem method [MMC],IConsoleNameSpace interface, IConsoleNameSpace interface [MMC],GetParentItem method, IConsoleNameSpace.GetParentItem, IConsoleNameSpace::GetParentItem, mmc.iconsolenamespace_getparentitem, mmc/IConsoleNameSpace::GetParentItem
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
 - IConsoleNameSpace.GetParentItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleNameSpace::GetParentItem


## -description


Enables the snap-in to retrieve the handle to a parent item in the scope view.


## -parameters




### -param item [in]

A handle to an item in the scope pane.


### -param pItemParent [out]

A pointer to the handle to the parent item that is returned.


### -param pCookie

TBD




#### - plCookie [out]

A pointer to the cookie associated with the parent item that is returned.


## -returns



This method can return one of these values.




## -remarks



If the given item has no parent, <b>NULL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/444bc86d-bfd2-435c-b9fb-691c4da92411">IConsoleNameSpace</a>
 

 

