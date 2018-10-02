---
UID: NF:mmc.IConsoleNameSpace.GetNextItem
title: IConsoleNameSpace::GetNextItem
author: windows-sdk-content
description: Enables the snap-in to retrieve the handle to the next item in the scope view.
old-location: mmc\iconsolenamespace_getnextitem.htm
tech.root: MMC
ms.assetid: E11BB91A-C0A3-4270-92B6-A05D24247B4A
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetNextItem, GetNextItem method [MMC], GetNextItem method [MMC],IConsoleNameSpace interface, IConsoleNameSpace interface [MMC],GetNextItem method, IConsoleNameSpace.GetNextItem, IConsoleNameSpace::GetNextItem, mmc.iconsolenamespace_getnextitem, mmc/IConsoleNameSpace::GetNextItem
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
 - IConsoleNameSpace.GetNextItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleNameSpace::GetNextItem


## -description


Enables the snap-in to retrieve the handle to the next item in the scope view.


## -parameters




### -param item [in]

A handle to an item in the scope pane.


### -param pItemNext [out]

A pointer to the handle to the next item in the scope pane that has been returned.


### -param pCookie

TBD




#### - plCookie [out]

A pointer to the cookie of the next item that has been returned.


## -returns



This method can return one of these values.




## -remarks



If there is no item next to the given item, <b>NULL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/444bc86d-bfd2-435c-b9fb-691c4da92411">IConsoleNameSpace</a>
 

 

