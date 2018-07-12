---
UID: NE:uiribbon.UI_EXECUTIONVERB
title: UI_EXECUTIONVERB
author: windows-sdk-content
description: Specifies values that identify the execution IDs that map to actions a user can initiate on a Command.
old-location: windowsribbon\windowsribbon_ui_executionverb.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_executionverb.htm
ms.author: windowssdkdev
ms.date: 05/09/2018
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


Specifies values that identify the execution IDs that map to actions a user can initiate on a <a href="https://msdn.microsoft.com/library/Dd371615(v=VS.85).aspx">Command</a>.  


## -enum-fields




### -field UI_EXECUTIONVERB_EXECUTE

Execute a command.


### -field UI_EXECUTIONVERB_PREVIEW

Show a preview of a visual element.


### -field UI_EXECUTIONVERB_CANCELPREVIEW

Cancel a preview of a visual element.


## -remarks



In the Ribbon framework, user actions are called executions. 

For example, if a user hovers the mouse over a gallery item,  UI_EXECUTIONVERB_PREVIEW is passed in a call to the <a href="https://msdn.microsoft.com/library/Dd371489(v=VS.85).aspx">IUICommandHandler::Execute</a> function of the gallery to indicate that  a live preview event occurred on the item.  If the user clicks the gallery item, UI_EXECUTIONVERB_EXECUTE is passed in a subsequent call to the <b>IUICommandHandler::Execute</b> function to indicate that the item was executed.




## -see-also




<a href="https://msdn.microsoft.com/library/Dd371540(v=VS.85).aspx">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/library/Dd316916(v=VS.85).aspx">Understanding Commands and Controls</a>



<a href="https://msdn.microsoft.com/library/Dd742868(v=VS.85).aspx">Working with Galleries</a>
 

 

