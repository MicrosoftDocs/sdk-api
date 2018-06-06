---
UID: NE:uiribbon.UI_EXECUTIONVERB
title: UI_EXECUTIONVERB
author: windows-sdk-content
description: Specifies values that identify the execution IDs that map to actions a user can initiate on a Command.
old-location: windowsribbon\windowsribbon_ui_executionverb.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_executionverb.htm
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: UI_EXECUTIONVERB, UI_EXECUTIONVERB enumeration [Windows Ribbon], UI_EXECUTIONVERB_CANCELPREVIEW, UI_EXECUTIONVERB_EXECUTE, UI_EXECUTIONVERB_PREVIEW, scenicintent_UI_EXECUTIONVERB, uiribbon/UI_EXECUTIONVERB, uiribbon/UI_EXECUTIONVERB_CANCELPREVIEW, uiribbon/UI_EXECUTIONVERB_EXECUTE, uiribbon/UI_EXECUTIONVERB_PREVIEW, windowsribbon.windowsribbon_ui_executionverb
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EXECUTIONVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_EXECUTIONVERB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

