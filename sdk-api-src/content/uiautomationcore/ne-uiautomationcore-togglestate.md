---
UID: NE:uiautomationcore.ToggleState
title: ToggleState (uiautomationcore.h)
description: Contains values that specify the toggle state of a Microsoft UI Automation element that implements the Toggle control pattern.
helpviewer_keywords: ["ToggleState","ToggleState enumeration [Windows Accessibility]","ToggleState_Indeterminate","ToggleState_Off","ToggleState_On","uiauto.uiauto_ToggleState","uiauto_ToggleState","uiautomationcore/ToggleState","uiautomationcore/ToggleState_Indeterminate","uiautomationcore/ToggleState_Off","uiautomationcore/ToggleState_On","winauto.uiauto_ToggleState"]
old-location: winauto\uiauto_ToggleState.htm
tech.root: WinAuto
ms.assetid: 242031d6-2d55-478d-b029-5a3b0a251601
ms.date: 12/05/2018
ms.keywords: ToggleState, ToggleState enumeration [Windows Accessibility], ToggleState_Indeterminate, ToggleState_Off, ToggleState_On, uiauto.uiauto_ToggleState, uiauto_ToggleState, uiautomationcore/ToggleState, uiautomationcore/ToggleState_Indeterminate, uiautomationcore/ToggleState_Off, uiautomationcore/ToggleState_On, winauto.uiauto_ToggleState
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
 - ToggleState
 - uiautomationcore/ToggleState
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
 - ToggleState
---

# ToggleState enumeration


## -description

Contains values that specify the toggle state of a Microsoft UI Automation element that implements the 
		<a href="/windows/desktop/WinAuto/uiauto-implementingtoggle">Toggle</a> <i>control pattern</i>.

## -enum-fields

### -field ToggleState_Off:0

The UI Automation element is not selected, checked, marked or otherwise activated.

### -field ToggleState_On:1

The UI Automation element is selected, checked, marked or otherwise activated.

### -field ToggleState_Indeterminate:2

The UI Automation element is in an indeterminate state. 
            

The Indeterminate property can be used to indicate whether the user has acted 
            on a control. For example, a check box can appear checked and dimmed, indicating an indeterminate state.
            

Creating an indeterminate state is different from disabling the control. 
            Consequently, a check box in the indeterminate state can still receive the focus. 
            When the user clicks an indeterminate control the ToggleState cycles to its next value.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itoggleprovider-toggle">Toggle</a>
