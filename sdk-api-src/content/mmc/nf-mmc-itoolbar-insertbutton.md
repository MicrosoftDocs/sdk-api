---
UID: NF:mmc.IToolbar.InsertButton
title: IToolbar::InsertButton
author: windows-sdk-content
description: Enables a snap-in to add a single button to the toolbar.
old-location: mmc\itoolbar_insertbutton.htm
tech.root: mmc
ms.assetid: 768df6d0-c2e5-4099-b4a6-a71e4f7e06d7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IToolbar interface [MMC],InsertButton method, IToolbar.InsertButton, IToolbar::InsertButton, InsertButton, InsertButton method [MMC], InsertButton method [MMC],IToolbar interface, _slate_itoolbar_insertbutton, mmc.itoolbar_insertbutton, mmc/IToolbar::InsertButton
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
 - IToolbar.InsertButton
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToolbar::InsertButton


## -description


The <b>IToolbar::InsertButton</b> method enables a snap-in to add a single button to the toolbar. The button being added is placed at the end of the toolbar.


## -parameters




### -param nIndex [in]

An internal index at which the button will be inserted. The button is always placed at the end of the toolbar; the internal index is required if the button is to be deleted (by means of 
<a href="https://msdn.microsoft.com/c893b3a6-a0f8-42ce-bf82-2e45f6458500">IToolbar::DeleteButton</a>).


### -param lpButton [in]

A pointer to the 
<a href="https://msdn.microsoft.com/340fed49-3003-4dd6-80c9-6cefc8c5b750">MMCBUTTON</a> structure that defines the button to be inserted.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

