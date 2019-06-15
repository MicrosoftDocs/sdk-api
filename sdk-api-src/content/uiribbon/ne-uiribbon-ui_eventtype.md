---
UID: NE:uiribbon.UI_EVENTTYPE
title: UI_EVENTTYPE (uiribbon.h)
author: windows-sdk-content
description: Identifies the types of events associated with a Ribbon.
old-location: windowsribbon\ui_eventtype.htm
tech.root: windowsribbon
ms.assetid: 424C833C-E6D6-4532-8CF1-A294B429CC21
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# UI_EVENTTYPE enumeration


## -description


Identifies the types of events associated with a <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a>.


## -enum-fields




### -field UI_EVENTTYPE_ApplicationMenuOpened

The <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-applicationmenu">ApplicationMenu</a> opened.


### -field UI_EVENTTYPE_RibbonMinimized

The <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a> minimized.


### -field UI_EVENTTYPE_RibbonExpanded

The <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a> expanded.


### -field UI_EVENTTYPE_ApplicationModeSwitched

The <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/ribbon-applicationmodes">application mode</a> changed.


### -field UI_EVENTTYPE_TabActivated

A <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-tab">Tab</a> activated.


### -field UI_EVENTTYPE_MenuOpened

A menu opened.


### -field UI_EVENTTYPE_CommandExecuted

A <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> executed.


### -field UI_EVENTTYPE_TooltipShown

A <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> tooltip displayed.


## -remarks



<b>UI_EVENTTYPE_TabActivated</b> is fired for both core tabs and contextual tabs; the <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a> event system does not distinguish between the two.

<b>UI_EVENTTYPE_MenuOpened</b> and <b>UI_EVENTTYPE_MenuClosed</b> are fired when either a regular menu or a gallery menu is opened or closed.

No event is fired when the <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-quickaccesstoolbar">QuickAccessToolbar</a> menu is opened or closed.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuieventlogger-onuievent">OnUIEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventlocation">UI_EVENTLOCATION</a>
 

 

