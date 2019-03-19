---
UID: NF:mmc.IConsole.SetToolbar
title: IConsole::SetToolbar (mmc.h)
author: windows-sdk-content
description: Sets the toolbar interface to be used for this instance of IComponent. Be aware that this is used only by instances of IComponent.
old-location: mmc\iconsole_settoolbar.htm
tech.root: mmc
ms.assetid: 242F3143-A6C1-49A1-A51B-735EE5D5D353
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IConsole interface [MMC],SetToolbar method, IConsole.SetToolbar, IConsole::SetToolbar, SetToolbar, SetToolbar method [MMC], SetToolbar method [MMC],IConsole interface, mmc.iconsole_settoolbar, mmc/IConsole::SetToolbar
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
 - IConsole.SetToolbar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsole::SetToolbar


## -description


Sets the toolbar interface to be used for this instance of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>. Be aware that this is used only by instances of 
<b>IComponent</b>.


## -parameters




### -param pToolbar [in]

A pointer to the 
<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a> interface.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt300830(v=VS.85).aspx">IConsole</a>



<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

