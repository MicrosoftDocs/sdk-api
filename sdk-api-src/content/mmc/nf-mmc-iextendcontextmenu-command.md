---
UID: NF:mmc.IExtendContextMenu.Command
title: IExtendContextMenu::Command (mmc.h)
author: windows-sdk-content
description: The IExtendContextMenu::Command method is called if one of the items you added to the context menu with IExtendContextMenu::AddMenuItems is subsequently selected.
old-location: mmc\iextendcontextmenu_command.htm
tech.root: mmc
ms.assetid: ee91a737-c6b4-48a1-88a2-57bef3730f5e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Command, Command method [MMC], Command method [MMC],IExtendContextMenu interface, IExtendContextMenu interface [MMC],Command method, IExtendContextMenu.Command, IExtendContextMenu::Command, _slate_iextendcontextmenu_command, mmc.iextendcontextmenu_command, mmc/IExtendContextMenu::Command
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendContextMenu.Command
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExtendContextMenu::Command


## -description


The <b>IExtendContextMenu::Command</b> method is called if one of the items you added to the context menu with 
<a href="https://msdn.microsoft.com/d4fc7bfd-b017-466e-81f2-74f13aec4b52">IExtendContextMenu::AddMenuItems</a> is subsequently selected. MMC calls 
Command with the command ID you specified and another pointer to the same 
<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a> interface.


## -parameters




### -param lCommandID [in]

A value that specifies the command identifier of the menu item.


### -param piDataObject [in]

A pointer to the 
<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a> interface on the object whose context menu was displayed.


## -returns



This method can return one of these values.




## -remarks



MMC reserves negative-valued command IDs for predefined menu command IDs that it sends to a snap-in's IExtendContextMenu::Command method. The –1 command ID is the MMCC_STANDARD_VIEW_SELECT enumerator value defined in mmc.h. This is sent to IExtendContextMenu::Command when the user clicks a standard view command on the 
<b>View</b> menu (Large, Small, List, or Detail). This notifies the snap-in that the user is switching away from a custom view (OCX, HTML). After getting an MMCC_STANDARD_VIEW_SELECT command, the snap-in should request a standard view the next time its 
<a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">IComponent::GetResultViewType</a> method is called and not request a custom view until one of its custom view menu items is selected. If the snap-in only uses standard views or only uses custom views, it can ignore the MMCC_STANDARD_VIEW_SELECT command.

MMC sends the snap-in the MMCC_STANDARD_VIEW_SELECT command when the user clicks the 
<b>Back</b> button on the toolbar. MMC uses this command to instruct the snap-in to display the result pane's previous view.




## -see-also




<a href="https://msdn.microsoft.com/58a0b4cf-0379-48a1-80c6-5245022cf891">CONTEXTMENUITEM</a>



<a href="https://msdn.microsoft.com/141a650f-a829-47b1-abf9-427302d98444">IContextMenuCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a>



<a href="https://msdn.microsoft.com/8fa4434e-ccdc-43fb-877e-a6f6a5fc95b2">IExtendContextMenu</a>



<a href="https://msdn.microsoft.com/b76b40da-1ab7-4b43-9c7e-03b901a6db3f">Working with Context Menus</a>
 

 

