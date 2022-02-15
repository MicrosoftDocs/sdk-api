---
UID: NE:uiribbon.UI_EVENTTYPE
title: UI_EVENTTYPE (uiribbon.h)
description: Identifies the types of events associated with a Ribbon.
helpviewer_keywords: ["UI_EVENTTYPE","UI_EVENTTYPE enumeration [Windows Ribbon]","UI_EVENTTYPE_ApplicationMenuOpened","UI_EVENTTYPE_ApplicationModeSwitched","UI_EVENTTYPE_CommandExecuted","UI_EVENTTYPE_MenuOpened","UI_EVENTTYPE_RibbonExpanded","UI_EVENTTYPE_RibbonMinimized","UI_EVENTTYPE_TabActivated","UI_EVENTTYPE_TooltipShown","uiribbon/UI_EVENTTYPE","uiribbon/UI_EVENTTYPE_ApplicationMenuOpened","uiribbon/UI_EVENTTYPE_ApplicationModeSwitched","uiribbon/UI_EVENTTYPE_CommandExecuted","uiribbon/UI_EVENTTYPE_MenuOpened","uiribbon/UI_EVENTTYPE_RibbonExpanded","uiribbon/UI_EVENTTYPE_RibbonMinimized","uiribbon/UI_EVENTTYPE_TabActivated","uiribbon/UI_EVENTTYPE_TooltipShown","windowsribbon.ui_eventtype"]
old-location: windowsribbon\ui_eventtype.htm
tech.root: windowsribbon
ms.assetid: 424C833C-E6D6-4532-8CF1-A294B429CC21
ms.date: 12/05/2018
ms.keywords: UI_EVENTTYPE, UI_EVENTTYPE enumeration [Windows Ribbon], UI_EVENTTYPE_ApplicationMenuOpened, UI_EVENTTYPE_ApplicationModeSwitched, UI_EVENTTYPE_CommandExecuted, UI_EVENTTYPE_MenuOpened, UI_EVENTTYPE_RibbonExpanded, UI_EVENTTYPE_RibbonMinimized, UI_EVENTTYPE_TabActivated, UI_EVENTTYPE_TooltipShown, uiribbon/UI_EVENTTYPE, uiribbon/UI_EVENTTYPE_ApplicationMenuOpened, uiribbon/UI_EVENTTYPE_ApplicationModeSwitched, uiribbon/UI_EVENTTYPE_CommandExecuted, uiribbon/UI_EVENTTYPE_MenuOpened, uiribbon/UI_EVENTTYPE_RibbonExpanded, uiribbon/UI_EVENTTYPE_RibbonMinimized, uiribbon/UI_EVENTTYPE_TabActivated, uiribbon/UI_EVENTTYPE_TooltipShown, windowsribbon.ui_eventtype
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
targetos: Windows
req.typenames: UI_EVENTTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_EVENTTYPE
 - uiribbon/UI_EVENTTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_EVENTTYPE
---

# UI_EVENTTYPE enumeration


## -description

Identifies the types of events associated with a <a href="/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a>.

## -enum-fields

### -field UI_EVENTTYPE_ApplicationMenuOpened:0

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-applicationmenu">ApplicationMenu</a> opened.

### -field UI_EVENTTYPE_RibbonMinimized:1

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a> minimized.

### -field UI_EVENTTYPE_RibbonExpanded:2

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a> expanded.

### -field UI_EVENTTYPE_ApplicationModeSwitched:3

The <a href="/windows/desktop/windowsribbon/ribbon-applicationmodes">application mode</a> changed.

### -field UI_EVENTTYPE_TabActivated:4

A <a href="/windows/desktop/windowsribbon/windowsribbon-element-tab">Tab</a> activated.

### -field UI_EVENTTYPE_MenuOpened:5

A menu opened.

### -field UI_EVENTTYPE_CommandExecuted:6

A <a href="/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> executed.

### -field UI_EVENTTYPE_TooltipShown:7

A <a href="/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> tooltip displayed.

## -remarks

<b>UI_EVENTTYPE_TabActivated</b> is fired for both core tabs and contextual tabs; the <a href="/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a> event system does not distinguish between the two.

<b>UI_EVENTTYPE_MenuOpened</b> and <b>UI_EVENTTYPE_MenuClosed</b> are fired when either a regular menu or a gallery menu is opened or closed.

No event is fired when the <a href="/windows/desktop/windowsribbon/windowsribbon-element-quickaccesstoolbar">QuickAccessToolbar</a> menu is opened or closed.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuieventlogger-onuievent">OnUIEvent</a>



<a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventlocation">UI_EVENTLOCATION</a>
