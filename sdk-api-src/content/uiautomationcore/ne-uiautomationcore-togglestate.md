---
UID: NE:uiautomationcore.ToggleState
title: ToggleState
author: windows-sdk-content
description: Contains values that specify the toggle state of a Microsoft UI Automation element that implements the Toggle&#32;control pattern.
old-location: winauto\uiauto_ToggleState.htm
tech.root: WinAuto
ms.assetid: 242031d6-2d55-478d-b029-5a3b0a251601
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ToggleState, ToggleState enumeration [Windows Accessibility], ToggleState_Indeterminate, ToggleState_Off, ToggleState_On, uiauto.uiauto_ToggleState, uiauto_ToggleState, uiautomationcore/ToggleState, uiautomationcore/ToggleState_Indeterminate, uiautomationcore/ToggleState_Off, uiautomationcore/ToggleState_On, winauto.uiauto_ToggleState
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
 - ToggleState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ToggleState enumeration


## -description


Contains values that specify the toggle state of a Microsoft UI Automation element that implements the 
		<a href="https://msdn.microsoft.com/9fd1232b-199a-41e6-81b0-667c7e463d09">Toggle</a> <i>control pattern</i>.


## -enum-fields




### -field ToggleState_Off

The UI Automation element is not selected, checked, marked or otherwise activated. 


### -field ToggleState_On

The UI Automation element is selected, checked, marked or otherwise activated. 


### -field ToggleState_Indeterminate

The UI Automation element is in an indeterminate state. 
            

The Indeterminate property can be used to indicate whether the user has acted 
            on a control. For example, a check box can appear checked and dimmed, indicating an indeterminate state.
            

Creating an indeterminate state is different from disabling the control. 
            Consequently, a check box in the indeterminate state can still receive the focus. 
            When the user clicks an indeterminate control the ToggleState cycles to its next value. 
            


## -see-also




<a href="https://msdn.microsoft.com/afadbcaf-156f-496e-a0f3-900e7f8d44da">Toggle</a>
 

 

