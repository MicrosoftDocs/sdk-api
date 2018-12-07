---
UID: NF:mmc.IToolbar.AddButtons
title: IToolbar::AddButtons
author: windows-sdk-content
description: Enables a snap-in to add an array of buttons to the toolbar.
old-location: mmc\itoolbar_addbuttons.htm
tech.root: mmc
ms.assetid: 9d37d0bc-d7c3-4d23-8dd4-c5a6c4af15ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddButtons, AddButtons method [MMC], AddButtons method [MMC],IToolbar interface, IToolbar interface [MMC],AddButtons method, IToolbar.AddButtons, IToolbar::AddButtons, _slate_itoolbar_addbuttons, mmc.itoolbar_addbuttons, mmc/IToolbar::AddButtons
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
 - IToolbar.AddButtons
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToolbar::AddButtons


## -description


The <b>IToolbar::AddButtons</b> method enables a snap-in to add an array of buttons to the toolbar.


## -parameters




### -param nButtons [in]

The number of buttons in the array.


### -param lpButtons [in]

A pointer to the 
<a href="https://msdn.microsoft.com/340fed49-3003-4dd6-80c9-6cefc8c5b750">MMCBUTTON</a> structure that contains information necessary for creating a button on the toolbar.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

