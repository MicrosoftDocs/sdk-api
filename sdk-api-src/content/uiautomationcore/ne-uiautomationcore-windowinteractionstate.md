---
UID: NE:uiautomationcore.WindowInteractionState
title: WindowInteractionState (uiautomationcore.h)
description: Contains values that specify the current state of the window for purposes of user interaction.
helpviewer_keywords: ["WindowInteractionState","WindowInteractionState enumeration [Windows Accessibility]","WindowInteractionState_BlockedByModalWindow","WindowInteractionState_Closing","WindowInteractionState_NotResponding","WindowInteractionState_ReadyForUserInteraction","WindowInteractionState_Running","uiauto.uiauto_WindowInteractionStateEnum","uiauto_WindowInteractionStateEnum","uiautomationcore/WindowInteractionState","uiautomationcore/WindowInteractionState_BlockedByModalWindow","uiautomationcore/WindowInteractionState_Closing","uiautomationcore/WindowInteractionState_NotResponding","uiautomationcore/WindowInteractionState_ReadyForUserInteraction","uiautomationcore/WindowInteractionState_Running","winauto.uiauto_WindowInteractionStateEnum"]
old-location: winauto\uiauto_WindowInteractionStateEnum.htm
tech.root: WinAuto
ms.assetid: 143e7262-42a9-4b1c-a8a3-5559befed02b
ms.date: 12/05/2018
ms.keywords: WindowInteractionState, WindowInteractionState enumeration [Windows Accessibility], WindowInteractionState_BlockedByModalWindow, WindowInteractionState_Closing, WindowInteractionState_NotResponding, WindowInteractionState_ReadyForUserInteraction, WindowInteractionState_Running, uiauto.uiauto_WindowInteractionStateEnum, uiauto_WindowInteractionStateEnum, uiautomationcore/WindowInteractionState, uiautomationcore/WindowInteractionState_BlockedByModalWindow, uiautomationcore/WindowInteractionState_Closing, uiautomationcore/WindowInteractionState_NotResponding, uiautomationcore/WindowInteractionState_ReadyForUserInteraction, uiautomationcore/WindowInteractionState_Running, winauto.uiauto_WindowInteractionStateEnum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WindowInteractionState
 - uiautomationcore/WindowInteractionState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - WindowInteractionState
---

# WindowInteractionState enumeration


## -description

Contains values that specify the current state of the window for purposes of user interaction.

## -enum-fields

### -field WindowInteractionState_Running:0

The window is running. This does not guarantee that the window is ready for user interaction or is responding.

### -field WindowInteractionState_Closing:1

The window is closing.

### -field WindowInteractionState_ReadyForUserInteraction:2

The window is ready for user interaction.

### -field WindowInteractionState_BlockedByModalWindow:3

The window is blocked by a modal window.

### -field WindowInteractionState_NotResponding:4

The window is not responding.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iwindowprovider">IWindowProvider</a>
