---
UID: NE:mmc._MMC_BUTTON_STATE
title: "_MMC_BUTTON_STATE"
author: windows-sdk-content
description: The MMC_BUTTON_STATE enumeration defines the possible states of buttons available in MMC. These values are used in the nState parameter of IConsoleVerb::GetVerbState, IConsoleVerb::SetVerbState, IToolbar::GetButtonState, and IToolbar::SetButtonState.
old-location: mmc\mmc_button_state.htm
tech.root: mmc
ms.assetid: b08c8905-1a6d-485f-9136-d63efd0e8194
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: BUTTONPRESSED, CHECKED, ENABLED, HIDDEN, INDETERMINATE, MMC_BUTTON_STATE, MMC_BUTTON_STATE enumeration [MMC], _MMC_BUTTON_STATE, _slate_mmc_button_state, mmc.mmc_button_state, mmc/BUTTONPRESSED, mmc/CHECKED, mmc/ENABLED, mmc/HIDDEN, mmc/INDETERMINATE, mmc/MMC_BUTTON_STATE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Mmc.h
api_name:
 - MMC_BUTTON_STATE
product: Windows
targetos: Windows
req.typenames: MMC_BUTTON_STATE
req.redist: 
---

# _MMC_BUTTON_STATE enumeration


## -description


The 
<b>MMC_BUTTON_STATE</b> enumeration defines the possible states of buttons available in MMC. These values are used in the <i>nState</i> parameter of 
<a href="https://msdn.microsoft.com/86388a22-5156-45e9-a601-33b7c5ca15f3">IConsoleVerb::GetVerbState</a>, 
<a href="https://msdn.microsoft.com/55cf5f73-a113-430e-be16-d7a88abe15b6">IConsoleVerb::SetVerbState</a>, 
<a href="https://msdn.microsoft.com/94c41b13-f1ab-4368-8cfa-960caeea796e">IToolbar::GetButtonState</a>, and 
<a href="https://msdn.microsoft.com/aa43fc1b-cc6d-474d-9b92-556924fb98de">IToolbar::SetButtonState</a>.


## -enum-fields




### -field ENABLED

The button accepts user input. A button that does not have this state does not accept user input and appears dimmed.


### -field CHECKED

The button has the CHECKED style and is being pressed.


### -field HIDDEN

The button is not visible and cannot receive user input.


### -field INDETERMINATE

The button appears dimmed.


### -field BUTTONPRESSED

The button is being pressed.

