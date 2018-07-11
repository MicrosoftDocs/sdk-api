---
UID: NF:mmc.IConsole.SetToolbar
title: IConsole::SetToolbar
author: windows-sdk-content
description: The IConsole2::SetToolbar method sets the toolbar interface to be used for this instance of IComponent. Be aware that this is used only by instances of IComponent.
old-location: mmc\iconsole2_settoolbar.htm
old-project: mmc
ms.assetid: c7a6d5ae-2541-4f64-8cc8-32ba2ae12605
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IConsole interface [MMC],SetToolbar method, IConsole.SetToolbar, IConsole2 interface [MMC],SetToolbar method, IConsole2::SetToolbar, IConsole3 interface [MMC],SetToolbar method, IConsole3::SetToolbar, IConsole::SetToolbar, SetToolbar, SetToolbar method [MMC], SetToolbar method [MMC],IConsole interface, SetToolbar method [MMC],IConsole2 interface, SetToolbar method [MMC],IConsole3 interface, _slate_iconsole2_settoolbar, mmc.iconsole2_settoolbar, mmc/IConsole2::SetToolbar, mmc/IConsole3::SetToolbar, mmc/IConsole::SetToolbar
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
 - IConsole2.SetToolbar
 - IConsole.SetToolbar
 - IConsole3.SetToolbar
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsole::SetToolbar


## -description


The <b>IConsole2::SetToolbar</b> method sets the toolbar interface to be used for this instance of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>. Be aware that this is used only by instances of 
<b>IComponent</b>.


## -parameters




### -param pToolbar [in]

A pointer to the 
<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a> interface.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>



<a href="https://msdn.microsoft.com/be3d42a4-a18a-40a5-99fc-2cf2a848c564">IConsole3</a>



<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

