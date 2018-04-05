---
UID: NE:uiribbon.UI_EVENTTYPE
title: UI_EVENTTYPE
author: windows-driver-content
description: Identifies the types of events associated with a Ribbon.
old-location: windowsribbon\ui_eventtype.htm
old-project: windowsribbon
ms.assetid: 424C833C-E6D6-4532-8CF1-A294B429CC21
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: UI_EVENTTYPE, UI_EVENTTYPE enumeration [Windows Ribbon], UI_EVENTTYPE_ApplicationMenuOpened, UI_EVENTTYPE_ApplicationModeSwitched, UI_EVENTTYPE_CommandExecuted, UI_EVENTTYPE_MenuOpened, UI_EVENTTYPE_RibbonExpanded, UI_EVENTTYPE_RibbonMinimized, UI_EVENTTYPE_TabActivated, UI_EVENTTYPE_TooltipShown, uiribbon/UI_EVENTTYPE, uiribbon/UI_EVENTTYPE_ApplicationMenuOpened, uiribbon/UI_EVENTTYPE_ApplicationModeSwitched, uiribbon/UI_EVENTTYPE_CommandExecuted, uiribbon/UI_EVENTTYPE_MenuOpened, uiribbon/UI_EVENTTYPE_RibbonExpanded, uiribbon/UI_EVENTTYPE_RibbonMinimized, uiribbon/UI_EVENTTYPE_TabActivated, uiribbon/UI_EVENTTYPE_TooltipShown, windowsribbon.ui_eventtype
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UI_EVENTTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Uiribbon.h
api_name:
-	UI_EVENTTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UI_EVENTTYPE enumeration


## -description


Identifies the types of events associated with a <a href="https://msdn.microsoft.com/51083180-4e86-4c90-9fd1-a58c12bcc756">Ribbon</a>.


## -enum-fields




### -field UI_EVENTTYPE_ApplicationMenuOpened

The <a href="https://msdn.microsoft.com/815e0462-ea45-44b1-81bf-f5797b22e920">ApplicationMenu</a> opened.


### -field UI_EVENTTYPE_RibbonMinimized

The <a href="https://msdn.microsoft.com/51083180-4e86-4c90-9fd1-a58c12bcc756">Ribbon</a> minimized.


### -field UI_EVENTTYPE_RibbonExpanded

The <a href="https://msdn.microsoft.com/51083180-4e86-4c90-9fd1-a58c12bcc756">Ribbon</a> expanded.


### -field UI_EVENTTYPE_ApplicationModeSwitched

The <a href="https://msdn.microsoft.com/8e9d85c5-33e4-4212-b9e4-2fc3b492c273">application mode</a> changed.


### -field UI_EVENTTYPE_TabActivated

A <a href="https://msdn.microsoft.com/2e73a89c-4d31-4075-93c8-e43213a20791">Tab</a> activated.


### -field UI_EVENTTYPE_MenuOpened

A menu opened.


### -field UI_EVENTTYPE_CommandExecuted

A <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a> executed.


### -field UI_EVENTTYPE_TooltipShown

A <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a> tooltip displayed.


## -remarks



<b>UI_EVENTTYPE_TabActivated</b> is fired for both core tabs and contextual tabs; the <a href="https://msdn.microsoft.com/51083180-4e86-4c90-9fd1-a58c12bcc756">Ribbon</a> event system does not distinguish between the two.

<b>UI_EVENTTYPE_MenuOpened</b> and <b>UI_EVENTTYPE_MenuClosed</b> are fired when either a regular menu or a gallery menu is opened or closed.

No event is fired when the <a href="https://msdn.microsoft.com/59aa35c3-a844-46b3-b066-c9a321fb0891">QuickAccessToolbar</a> menu is opened or closed.





## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/1BE6F914-C57D-4A8F-A286-C47BFD48B310">OnUIEvent</a>



<a href="https://msdn.microsoft.com/EA278262-8CA7-42A3-9F66-0C7B4D3AA525">UI_EVENTLOCATION</a>
 

 

