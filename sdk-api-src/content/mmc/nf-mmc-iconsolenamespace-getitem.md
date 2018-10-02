---
UID: NF:mmc.IConsoleNameSpace.GetItem
title: IConsoleNameSpace::GetItem
author: windows-sdk-content
description: Enables the snap-in to retrieve some or all of a single scope item's attributes.
old-location: mmc\iconsolenamespace_getitem.htm
tech.root: MMC
ms.assetid: 76E3188E-F046-489E-8A0E-CC8440E74D99
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetItem, GetItem method [MMC], GetItem method [MMC],IConsoleNameSpace interface, IConsoleNameSpace interface [MMC],GetItem method, IConsoleNameSpace.GetItem, IConsoleNameSpace::GetItem, mmc.iconsolenamespace_getitem, mmc/IConsoleNameSpace::GetItem
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
 - IConsoleNameSpace.GetItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleNameSpace::GetItem


## -description


Enables the snap-in to retrieve some or all of a single scope item's attributes.


## -parameters




### -param item [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c392f25c-80e7-4c91-9063-36143320b9aa">SCOPEDATAITEM</a> structure that specifies the information to retrieve and receives information about the item. When the message is sent, the 
ID member of the structure identifies the item and the mask member specifies the attributes to retrieve.

If mask specifies the <b>SDI_STATE</b> value, the <b>nState</b> member contains the item's state information.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/444bc86d-bfd2-435c-b9fb-691c4da92411">IConsoleNameSpace</a>
 

 

