---
UID: NE:uiribbon.UI_EVENTTYPE
title: UI_EVENTTYPE
author: windows-sdk-content
description: Identifies the types of events associated with a Ribbon.
old-location: windowsribbon\ui_eventtype.htm
tech.root: windowsribbon
ms.assetid: 424C833C-E6D6-4532-8CF1-A294B429CC21
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UI_EVENTTYPE, UI_EVENTTYPE enumeration [Windows Ribbon], UI_EVENTTYPE_ApplicationMenuOpened, UI_EVENTTYPE_ApplicationModeSwitched, UI_EVENTTYPE_CommandExecuted, UI_EVENTTYPE_MenuOpened, UI_EVENTTYPE_RibbonExpanded, UI_EVENTTYPE_RibbonMinimized, UI_EVENTTYPE_TabActivated, UI_EVENTTYPE_TooltipShown, uiribbon/UI_EVENTTYPE, uiribbon/UI_EVENTTYPE_ApplicationMenuOpened, uiribbon/UI_EVENTTYPE_ApplicationModeSwitched, uiribbon/UI_EVENTTYPE_CommandExecuted, uiribbon/UI_EVENTTYPE_MenuOpened, uiribbon/UI_EVENTTYPE_RibbonExpanded, uiribbon/UI_EVENTTYPE_RibbonMinimized, uiribbon/UI_EVENTTYPE_TabActivated, uiribbon/UI_EVENTTYPE_TooltipShown, windowsribbon.ui_eventtype
ms.topic: enum
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_EVENTTYPE
product: Windows
targetos: Windows
req.typenames: UI_EVENTTYPE
req.redist: 
---

# UI_EVENTTYPE enumeration


## -description


Identifies the types of events associated with a <a href="https://msdn.microsoft.com/en-us/library/Dd316811(v=VS.85).aspx">Ribbon</a>.


## -enum-fields




### -field UI_EVENTTYPE_ApplicationMenuOpened

The <a href="https://msdn.microsoft.com/en-us/library/Dd371601(v=VS.85).aspx">ApplicationMenu</a> opened.


### -field UI_EVENTTYPE_RibbonMinimized

The <a href="https://msdn.microsoft.com/en-us/library/Dd316811(v=VS.85).aspx">Ribbon</a> minimized.


### -field UI_EVENTTYPE_RibbonExpanded

The <a href="https://msdn.microsoft.com/en-us/library/Dd316811(v=VS.85).aspx">Ribbon</a> expanded.


### -field UI_EVENTTYPE_ApplicationModeSwitched

The <a href="https://msdn.microsoft.com/en-us/library/Dd940486(v=VS.85).aspx">application mode</a> changed.


### -field UI_EVENTTYPE_TabActivated

A <a href="https://msdn.microsoft.com/en-us/library/Dd316894(v=VS.85).aspx">Tab</a> activated.


### -field UI_EVENTTYPE_MenuOpened

A menu opened.


### -field UI_EVENTTYPE_CommandExecuted

A <a href="https://msdn.microsoft.com/en-us/library/Dd371615(v=VS.85).aspx">Command</a> executed.


### -field UI_EVENTTYPE_TooltipShown

A <a href="https://msdn.microsoft.com/en-us/library/Dd371615(v=VS.85).aspx">Command</a> tooltip displayed.


## -remarks



<b>UI_EVENTTYPE_TabActivated</b> is fired for both core tabs and contextual tabs; the <a href="https://msdn.microsoft.com/en-us/library/Dd316811(v=VS.85).aspx">Ribbon</a> event system does not distinguish between the two.

<b>UI_EVENTTYPE_MenuOpened</b> and <b>UI_EVENTTYPE_MenuClosed</b> are fired when either a regular menu or a gallery menu is opened or closed.

No event is fired when the <a href="https://msdn.microsoft.com/en-us/library/Dd371713(v=VS.85).aspx">QuickAccessToolbar</a> menu is opened or closed.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371540(v=VS.85).aspx">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/1BE6F914-C57D-4A8F-A286-C47BFD48B310">OnUIEvent</a>



<a href="https://msdn.microsoft.com/EA278262-8CA7-42A3-9F66-0C7B4D3AA525">UI_EVENTLOCATION</a>
 

 

