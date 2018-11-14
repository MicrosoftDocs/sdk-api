---
UID: NS:uiribbon._UI_EVENTPARAMS
title: "_UI_EVENTPARAMS"
author: windows-sdk-content
description: Contains information about a Ribbon event.
old-location: windowsribbon\ui_eventparams.htm
tech.root: windowsribbon
ms.assetid: 438ACF91-3C83-4E2D-B919-4CCAE65BCD3E
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PUI_EVENTPARAMS, PUI_EVENTPARAMS structure pointer [Windows Ribbon], UI_EVENTPARAMS, UI_EVENTPARAMS structure [Windows Ribbon], _UI_EVENTPARAMS, uiribbon/PUI_EVENTPARAMS, uiribbon/UI_EVENTPARAMS, windowsribbon.ui_eventparams
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
 - UI_EVENTPARAMS
product: Windows
targetos: Windows
req.typenames: UI_EVENTPARAMS
req.redist: 
---

# _UI_EVENTPARAMS structure


## -description


Contains information about a <a href="https://msdn.microsoft.com/51083180-4e86-4c90-9fd1-a58c12bcc756">Ribbon</a> event.


## -struct-fields




### -field EventType

One of the values from <a href="https://msdn.microsoft.com/424C833C-E6D6-4532-8CF1-A294B429CC21">UI_EVENTTYPE</a>.


### -field Modes

The application modes.


### -field Params

The <a href="https://msdn.microsoft.com/f332423d-d258-488d-9233-71687288b462">Command</a> associated with the event.


## -remarks



For top-level events (application menu opened/closed, ribbon minimized/expanded/pinned), <b>Modes</b> is present but set to zero (and can be ignored by the application).



For the <a href="https://msdn.microsoft.com/424C833C-E6D6-4532-8CF1-A294B429CC21">UI_EVENTTYPE_ApplicationModeSwitched</a> event,  <b>Modes</b> specifies which modes have been set.  (This is the same integer value that is passed to <a href="https://msdn.microsoft.com/5c55a1ac-b84b-4ccc-b4cc-ba5bebc2d78e">SetModes</a> to switch modes in the first place.)



For all other events, <b>Params</b> contains additional data about the event.




## -see-also




<a href="https://msdn.microsoft.com/1BE6F914-C57D-4A8F-A286-C47BFD48B310">OnUIEvent</a>



<a href="https://msdn.microsoft.com/8e9d85c5-33e4-4212-b9e4-2fc3b492c273">Reconfiguring the Ribbon with Application Modes</a>



<a href="https://msdn.microsoft.com/5c55a1ac-b84b-4ccc-b4cc-ba5bebc2d78e">SetModes</a>



<a href="https://msdn.microsoft.com/8A109C67-BF05-4BA4-8F12-473F2C773B90">Structures</a>
 

 

