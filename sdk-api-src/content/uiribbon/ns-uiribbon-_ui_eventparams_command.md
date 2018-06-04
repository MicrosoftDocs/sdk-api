---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>



<a href="https://msdn.microsoft.com/438ACF91-3C83-4E2D-B919-4CCAE65BCD3E">UI_EVENTPARAMS</a>
 

 

