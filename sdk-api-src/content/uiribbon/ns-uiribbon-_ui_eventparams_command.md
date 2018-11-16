---
UID: NS:uiribbon._UI_EVENTPARAMS_COMMAND
title: "_UI_EVENTPARAMS_COMMAND"
author: windows-sdk-content
description: Contains information about a Command associated with a event.
old-location: windowsribbon\ui_eventparams_command_.htm
tech.root: windowsribbon
ms.assetid: 7B1E92E2-DFFE-4B4F-87F1-1BFBD8E06D08
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PUI_EVENTPARAMS_COMMAND, PUI_EVENTPARAMS_COMMAND structure pointer [Windows Ribbon], UI_EVENTPARAMS_COMMAND, UI_EVENTPARAMS_COMMAND , UI_EVENTPARAMS_COMMAND structure [Windows Ribbon], _UI_EVENTPARAMS_COMMAND, uiribbon/PUI_EVENTPARAMS_COMMAND, uiribbon/UI_EVENTPARAMS_COMMAND, windowsribbon.ui_eventparams_command_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_EVENTPARAMS_COMMAND
product: Windows
targetos: Windows
req.typenames: UI_EVENTPARAMS_COMMAND
req.redist: 
---

# _UI_EVENTPARAMS_COMMAND structure


## -description


Contains information about a <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a> associated with a event.


## -struct-fields




### -field CommandID

The ID of the <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a> directly related to the event, which is specified in the markup resource file.
				


### -field CommandName

The <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a> name that is associated with <b>CommandId</b>.


### -field ParentCommandID

The ID for the parent of the <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a>, which is specified in the markup resource file.
				


### -field ParentCommandName

The <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a> name  of the parent that is associated with <b>CommandId</b>.


### -field SelectionIndex

<b>SelectionIndex</b> is used only when a <a href="https://msdn.microsoft.com/424C833C-E6D6-4532-8CF1-A294B429CC21">UI_EVENTTYPE_CommandExecuted</a> has been fired in response to the user selecting an item within a <a href="https://msdn.microsoft.com/d796e26b-44c2-4e11-b1a5-2ede5bcff676">ComboBox</a> or item gallery.  In those cases, <b>SelectionIndex</b> contains the index of the selected item.  In all other cases, it is set to 0.



### -field Location

One of the values from <a href="https://msdn.microsoft.com/EA278262-8CA7-42A3-9F66-0C7B4D3AA525">UI_EVENTLOCATION</a>.


## -remarks



 The Command identified by <b>CommandID</b> and <b>CommandName</b> depend upon which event has occurred:  for a <a href="https://msdn.microsoft.com/424C833C-E6D6-4532-8CF1-A294B429CC21">UI_EVENTTYPE_TabActivated</a> event, they identify the tab; for a <b>UI_EVENTTYPE_MenuOpened</b> event, they identify the menu; for <b>UI_EVENTTYPE_CommandExecuted</b> events, they identify the command being executed; and for <b>UI_EVENTTYPE_TooltipShown</b> events, they identify the <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a> that owns that tooltip.



<b>ParentCommandID</b> and <b>ParentCommandName</b>  identify the parent command (if any) of the command associated with this event.  If there is no parent, then <b>ParentCommandID</b> is zero and <b>ParentCommandName</b> is an empty string.






## -see-also




<a href="https://msdn.microsoft.com/1BE6F914-C57D-4A8F-A286-C47BFD48B310">OnUIEvent</a>



<a href="https://msdn.microsoft.com/8A109C67-BF05-4BA4-8F12-473F2C773B90">Structures</a>



<a href="https://msdn.microsoft.com/438ACF91-3C83-4E2D-B919-4CCAE65BCD3E">UI_EVENTPARAMS</a>
 

 

