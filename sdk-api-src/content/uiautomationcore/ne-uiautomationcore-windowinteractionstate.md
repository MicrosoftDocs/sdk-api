---
UID: NE:uiautomationcore.WindowInteractionState
title: WindowInteractionState
author: windows-sdk-content
description: Contains values that specify the current state of the window for purposes of user interaction.
old-location: winauto\uiauto_WindowInteractionStateEnum.htm
tech.root: WinAuto
ms.assetid: 143e7262-42a9-4b1c-a8a3-5559befed02b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WindowInteractionState, WindowInteractionState enumeration [Windows Accessibility], WindowInteractionState_BlockedByModalWindow, WindowInteractionState_Closing, WindowInteractionState_NotResponding, WindowInteractionState_ReadyForUserInteraction, WindowInteractionState_Running, uiauto.uiauto_WindowInteractionStateEnum, uiauto_WindowInteractionStateEnum, uiautomationcore/WindowInteractionState, uiautomationcore/WindowInteractionState_BlockedByModalWindow, uiautomationcore/WindowInteractionState_Closing, uiautomationcore/WindowInteractionState_NotResponding, uiautomationcore/WindowInteractionState_ReadyForUserInteraction, uiautomationcore/WindowInteractionState_Running, winauto.uiauto_WindowInteractionStateEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - UIAutomationCore.h
api_name:
 - WindowInteractionState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WindowInteractionState enumeration


## -description


Contains values that specify the current state of the window for purposes of user interaction.


## -enum-fields




### -field WindowInteractionState_Running

The window is running. This does not guarantee that the window is ready for user interaction or is responding. 


### -field WindowInteractionState_Closing

The window is closing.


### -field WindowInteractionState_ReadyForUserInteraction

The window is ready for user interaction.


### -field WindowInteractionState_BlockedByModalWindow

The window is blocked by a modal window.


### -field WindowInteractionState_NotResponding

The window is not responding.


## -see-also




<a href="https://msdn.microsoft.com/cf09ad4e-fd5b-4304-b5fb-165205bff1f3">IWindowProvider</a>
 

 

