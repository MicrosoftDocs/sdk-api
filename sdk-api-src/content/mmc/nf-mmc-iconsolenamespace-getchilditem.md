---
UID: NF:mmc.IConsoleNameSpace.GetChildItem
title: IConsoleNameSpace::GetChildItem
author: windows-sdk-content
description: Enables the snap-in to get the handle to a child item in the scope pane.
old-location: mmc\iconsolenamespace_getchilditem.htm
tech.root: MMC
ms.assetid: 05929125-307C-48C5-A2EA-B1133C8EE66B
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetChildItem, GetChildItem method [MMC], GetChildItem method [MMC],IConsoleNameSpace interface, IConsoleNameSpace interface [MMC],GetChildItem method, IConsoleNameSpace.GetChildItem, IConsoleNameSpace::GetChildItem, mmc.iconsolenamespace_getchilditem, mmc/IConsoleNameSpace::GetChildItem
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
 - IConsoleNameSpace.GetChildItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleNameSpace::GetChildItem


## -description


Enables the snap-in to get the handle to a child item in the scope pane.


## -parameters




### -param item [in]

A handle to a parent item in the scope pane.


### -param pItemChild [out]

A pointer to the handle that identifies the child item in the scope pane that has been returned.


### -param pCookie

TBD




#### - plCookie [out]

A pointer to the cookie associated with the child item that has been returned.


## -returns



This method can return one of these values.




## -remarks



If the handle to the child item is not obtained, <b>NULL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/444bc86d-bfd2-435c-b9fb-691c4da92411">IConsoleNameSpace</a>
 

 

