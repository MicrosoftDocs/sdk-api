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

# UI_EXECUTIONVERB enumeration


## -description


Specifies values that identify the execution IDs that map to actions a user can initiate on a <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a>.  


## -enum-fields




### -field UI_EXECUTIONVERB_EXECUTE

Execute a command.


### -field UI_EXECUTIONVERB_PREVIEW

Show a preview of a visual element.


### -field UI_EXECUTIONVERB_CANCELPREVIEW

Cancel a preview of a visual element.


## -remarks



In the Ribbon framework, user actions are called executions. 

For example, if a user hovers the mouse over a gallery item,  UI_EXECUTIONVERB_PREVIEW is passed in a call to the <a href="https://msdn.microsoft.com/d4f3e260-2839-4f0b-892b-7e61f20238f3">IUICommandHandler::Execute</a> function of the gallery to indicate that  a live preview event occurred on the item.  If the user clicks the gallery item, UI_EXECUTIONVERB_EXECUTE is passed in a subsequent call to the <b>IUICommandHandler::Execute</b> function to indicate that the item was executed.




## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d">Understanding Commands and Controls</a>



<a href="https://msdn.microsoft.com/447039f3-1428-4b6f-94cf-78cf81974041">Working with Galleries</a>
 

 

