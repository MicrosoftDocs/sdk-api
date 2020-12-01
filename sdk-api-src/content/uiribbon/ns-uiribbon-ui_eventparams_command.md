---
UID: NS:uiribbon._UI_EVENTPARAMS_COMMAND
title: UI_EVENTPARAMS_COMMAND (uiribbon.h)
description: Contains information about a Command associated with a event.
helpviewer_keywords: ["PUI_EVENTPARAMS_COMMAND","PUI_EVENTPARAMS_COMMAND structure pointer [Windows Ribbon]","UI_EVENTPARAMS_COMMAND","UI_EVENTPARAMS_COMMAND","UI_EVENTPARAMS_COMMAND structure [Windows Ribbon]","uiribbon/PUI_EVENTPARAMS_COMMAND","uiribbon/UI_EVENTPARAMS_COMMAND","windowsribbon.ui_eventparams_command_"]
old-location: windowsribbon\ui_eventparams_command_.htm
tech.root: windowsribbon
ms.assetid: 7B1E92E2-DFFE-4B4F-87F1-1BFBD8E06D08
ms.date: 12/05/2018
ms.keywords: PUI_EVENTPARAMS_COMMAND, PUI_EVENTPARAMS_COMMAND structure pointer [Windows Ribbon], UI_EVENTPARAMS_COMMAND, UI_EVENTPARAMS_COMMAND , UI_EVENTPARAMS_COMMAND structure [Windows Ribbon], uiribbon/PUI_EVENTPARAMS_COMMAND, uiribbon/UI_EVENTPARAMS_COMMAND, windowsribbon.ui_eventparams_command_
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: UI_EVENTPARAMS_COMMAND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _UI_EVENTPARAMS_COMMAND
 - uiribbon/_UI_EVENTPARAMS_COMMAND
 - UI_EVENTPARAMS_COMMAND
 - uiribbon/UI_EVENTPARAMS_COMMAND
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
 - UI_EVENTPARAMS_COMMAND
---

# UI_EVENTPARAMS_COMMAND structure


## -description

Contains information about a <a href="/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> associated with a event.

## -struct-fields

### -field CommandID

The ID of the <a href="/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> directly related to the event, which is specified in the markup resource file.

### -field CommandName

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> name that is associated with <b>CommandId</b>.

### -field ParentCommandID

The ID for the parent of the <a href="/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a>, which is specified in the markup resource file.

### -field ParentCommandName

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> name  of the parent that is associated with <b>CommandId</b>.

### -field SelectionIndex

<b>SelectionIndex</b> is used only when a <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventtype">UI_EVENTTYPE_CommandExecuted</a> has been fired in response to the user selecting an item within a <a href="/windows/desktop/windowsribbon/windowsribbon-element-combobox">ComboBox</a> or item gallery.  In those cases, <b>SelectionIndex</b> contains the index of the selected item.  In all other cases, it is set to 0.

### -field Location

One of the values from <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventlocation">UI_EVENTLOCATION</a>.

## -remarks

 The Command identified by <b>CommandID</b> and <b>CommandName</b> depend upon which event has occurred:  for a <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventtype">UI_EVENTTYPE_TabActivated</a> event, they identify the tab; for a <b>UI_EVENTTYPE_MenuOpened</b> event, they identify the menu; for <b>UI_EVENTTYPE_CommandExecuted</b> events, they identify the command being executed; and for <b>UI_EVENTTYPE_TooltipShown</b> events, they identify the <a href="/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> that owns that tooltip.



<b>ParentCommandID</b> and <b>ParentCommandName</b>  identify the parent command (if any) of the command associated with this event.  If there is no parent, then <b>ParentCommandID</b> is zero and <b>ParentCommandName</b> is an empty string.

## -see-also

<a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuieventlogger-onuievent">OnUIEvent</a>



<a href="/windows/desktop/windowsribbon/structures">Structures</a>



<a href="/windows/desktop/api/uiribbon/ns-uiribbon-ui_eventparams">UI_EVENTPARAMS</a>