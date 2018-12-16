---
UID: NF:mmc.IContextMenuProvider.ShowContextMenu
title: IContextMenuProvider::ShowContextMenu
author: windows-sdk-content
description: The IContextMenuProvider::ShowContextMenu method displays a context menu.
old-location: mmc\icontextmenuprovider_showcontextmenu.htm
tech.root: mmc
ms.assetid: 8fe9f474-c47b-4b53-8cbc-d658c82d7591
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IContextMenuProvider interface [MMC],ShowContextMenu method, IContextMenuProvider.ShowContextMenu, IContextMenuProvider::ShowContextMenu, ShowContextMenu, ShowContextMenu method [MMC], ShowContextMenu method [MMC],IContextMenuProvider interface, _slate_icontextmenuprovider_showcontextmenu, mmc.icontextmenuprovider_showcontextmenu, mmc/IContextMenuProvider::ShowContextMenu
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
 - IContextMenuProvider.ShowContextMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContextMenuProvider::ShowContextMenu


## -description


The <b>IContextMenuProvider::ShowContextMenu</b> method displays a context menu.


## -parameters




### -param hwndParent [in]

A handle to the parent window in which the context menu is displayed.


### -param xPos [in]

A value, in screen coordinates, that specifies the horizontal location of the upper-left corner of the context menu, in screen coordinates.


### -param yPos [in]

A value, in screen coordinates, that specifies the vertical location of the upper-left corner of the context menu.


### -param plSelected [out]

A value that specifies the ICommandID value (as passed to 
<a href="https://msdn.microsoft.com/7186f201-13aa-4357-9b89-b435d244229c">IContextMenuCallback::AddItem</a>) of the selected menu item. If this is zero, either none of the context menu items were selected or the selected context menu item was added by an extension. If an extension item was selected, 
ShowContextMenu notifies the extension by calling 
<a href="https://msdn.microsoft.com/ee91a737-c6b4-48a1-88a2-57bef3730f5e">IExtendContextMenu::Command</a>.


## -returns



This method can return one of these values.




## -remarks



ShowContextMenu automatically clears the context menu after that displays it. A best practice is to call 
<a href="https://msdn.microsoft.com/d8867d95-4812-499b-81cd-d0f9471fe33b">IContextMenuProvider::EmptyMenuList</a> before beginning to build a context menu.




## -see-also




<a href="https://msdn.microsoft.com/3f9a5945-9b34-41fe-9c91-c782eb7eb739">IContextMenuProvider</a>
 

 

