---
UID: NF:mmc.IConsole.NewWindow
title: IConsole::NewWindow
author: windows-sdk-content
description: Creates a new multiple-document interface (MDI) child window rooted at the specified scope item.
old-location: mmc\iconsole_newwindow.htm
tech.root: mmc
ms.assetid: 78496DA1-1C8F-4C63-83E1-45FC0BC80779
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IConsole interface [MMC],NewWindow method, IConsole.NewWindow, IConsole::NewWindow, MMC_NW_OPTION_CUSTOMTITLE, MMC_NW_OPTION_NONE, MMC_NW_OPTION_NOPERSIST, MMC_NW_OPTION_NOSCOPEPANE, MMC_NW_OPTION_NOTOOLBARS, MMC_NW_OPTION_SHORTTITLE, NewWindow, NewWindow method [MMC], NewWindow method [MMC],IConsole interface, mmc.iconsole_newwindow, mmc/IConsole::NewWindow
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
 - IConsole.NewWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsole::NewWindow


## -description


Creates a new multiple-document interface (MDI) child window rooted at the specified scope item.


## -parameters




### -param hScopeItem [in]

The scope item that forms the root of the new window.


### -param lOptions [in]

Options used to create the new window are listed in the following list.



#### MMC_NW_OPTION_NONE

Display a new window with default window settings. This is the programmatic equivalent to selecting the New Window From Here command from the 
<b>View</b> context menu.



#### MMC_NW_OPTION_NOSCOPEPANE

Hide the scope pane (Console Tree pane) in the new window.



#### MMC_NW_OPTION_NOTOOLBARS

Hide the standard toolbars in the new window. If the snap-in has custom toolbar buttons and menus, they will appear.

If the snap-in has added its own items to standard menus or toolbars, the addition of those items does not force the standard toolbars or menus that contain them to appear.



#### MMC_NW_OPTION_SHORTTITLE

This option is not supported and its definition exists only for backward compatibility.



#### MMC_NW_OPTION_CUSTOMTITLE

Use the custom title provided by the snap-in. Title bar text contains the display name specified by the item data object implementation of the <b>CCF_DISPLAY_NAME</b>.



#### MMC_NW_OPTION_NOPERSIST

Do not save the new window to the .msc file.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt300830(v=VS.85).aspx">IConsole</a>
 

 

