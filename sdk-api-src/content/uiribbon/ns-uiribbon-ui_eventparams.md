---
UID: NS:uiribbon._UI_EVENTPARAMS
title: UI_EVENTPARAMS (uiribbon.h)
author: windows-sdk-content
description: Contains information about a Ribbon event.
old-location: windowsribbon\ui_eventparams.htm
tech.root: windowsribbon
ms.assetid: 438ACF91-3C83-4E2D-B919-4CCAE65BCD3E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PUI_EVENTPARAMS, PUI_EVENTPARAMS structure pointer [Windows Ribbon], UI_EVENTPARAMS, UI_EVENTPARAMS structure [Windows Ribbon], uiribbon/PUI_EVENTPARAMS, uiribbon/UI_EVENTPARAMS, windowsribbon.ui_eventparams
ms.topic: struct
f1_keywords: ["uiribbon/UI_EVENTPARAMS"]
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
ms.custom: 19H1
---

# UI_EVENTPARAMS structure


## -description


Contains information about a <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a> event.


## -struct-fields




### -field EventType

One of the values from <a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventtype">UI_EVENTTYPE</a>.


### -field Modes

The application modes.


### -field Params

The <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a> associated with the event.


## -remarks



For top-level events (application menu opened/closed, ribbon minimized/expanded/pinned), <b>Modes</b> is present but set to zero (and can be ignored by the application).



For the <a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventtype">UI_EVENTTYPE_ApplicationModeSwitched</a> event,  <b>Modes</b> specifies which modes have been set.  (This is the same integer value that is passed to <a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes">SetModes</a> to switch modes in the first place.)



For all other events, <b>Params</b> contains additional data about the event.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuieventlogger-onuievent">OnUIEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/ribbon-applicationmodes">Reconfiguring the Ribbon with Application Modes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes">SetModes</a>



<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/structures">Structures</a>
 

 

