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
 

 

