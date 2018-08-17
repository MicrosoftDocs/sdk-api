---
UID: NF:mmc.IConsole.SelectScopeItem
title: IConsole::SelectScopeItem
author: windows-sdk-content
description: Selects the given scope item.
old-location: mmc\iconsole_selectscopeitem.htm
old-project: mmc
ms.assetid: ADE56DDF-C437-4BF3-A2EC-1E35EE7567F3
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IConsole interface [MMC],SelectScopeItem method, IConsole.SelectScopeItem, IConsole::SelectScopeItem, SelectScopeItem, SelectScopeItem method [MMC], SelectScopeItem method [MMC],IConsole interface, mmc.iconsole_selectscopeitem, mmc/IConsole::SelectScopeItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
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
 - IConsole.SelectScopeItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsole::SelectScopeItem


## -description


Selects the given scope item.


## -parameters




### -param hScopeItem [in]

A handle to the item in the scope pane to be selected.


## -returns



This method can return one of these values.




## -remarks



Use this method to reselect the currently selected scope item or to select another scope item.

You can have a single scope item with several different views available, for example, several OLE custom control (OCX) views and the default list view. When the user selects a different view from a menu, the snap-in receives the command and should then call 
<b>SelectScopeItem</b> to reselect the item. 
<a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">IComponent::GetResultViewType</a> can then return the new view type.

If 
<b>SelectScopeItem</b> is called by the snap-in in its <a href="https://msdn.microsoft.com/de89a195-082b-4d5f-bd8c-1c75215ab60f">MMCN_EXPAND</a> notification handler, MMC will not select the specified scope item, even though 
<b>SelectScopeItem</b> may return <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt300830(v=VS.85).aspx">IConsole</a>
 

 

