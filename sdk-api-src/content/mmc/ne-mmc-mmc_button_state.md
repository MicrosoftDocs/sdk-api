---
UID: NE:mmc._MMC_BUTTON_STATE
title: MMC_BUTTON_STATE (mmc.h)
description: The MMC_BUTTON_STATE enumeration defines the possible states of buttons available in MMC. These values are used in the nState parameter of IConsoleVerb::GetVerbState, IConsoleVerb::SetVerbState, IToolbar::GetButtonState, and IToolbar::SetButtonState.
helpviewer_keywords: ["BUTTONPRESSED","CHECKED","ENABLED","HIDDEN","INDETERMINATE","MMC_BUTTON_STATE","MMC_BUTTON_STATE enumeration [MMC]","_slate_mmc_button_state","mmc.mmc_button_state","mmc/BUTTONPRESSED","mmc/CHECKED","mmc/ENABLED","mmc/HIDDEN","mmc/INDETERMINATE","mmc/MMC_BUTTON_STATE"]
old-location: mmc\mmc_button_state.htm
tech.root: mmc
ms.assetid: b08c8905-1a6d-485f-9136-d63efd0e8194
ms.date: 12/05/2018
ms.keywords: BUTTONPRESSED, CHECKED, ENABLED, HIDDEN, INDETERMINATE, MMC_BUTTON_STATE, MMC_BUTTON_STATE enumeration [MMC], _slate_mmc_button_state, mmc.mmc_button_state, mmc/BUTTONPRESSED, mmc/CHECKED, mmc/ENABLED, mmc/HIDDEN, mmc/INDETERMINATE, mmc/MMC_BUTTON_STATE
f1_keywords:
- mmc/MMC_BUTTON_STATE
dev_langs:
- c++
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
targetos: Windows
req.typenames: MMC_BUTTON_STATE
req.redist: 
ms.custom: 19H1
---

# MMC_BUTTON_STATE enumeration


## -description


The 
<b>MMC_BUTTON_STATE</b> enumeration defines the possible states of buttons available in MMC. These values are used in the <i>nState</i> parameter of 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsoleverb-getverbstate">IConsoleVerb::GetVerbState</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsoleverb-setverbstate">IConsoleVerb::SetVerbState</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-itoolbar-getbuttonstate">IToolbar::GetButtonState</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-itoolbar-setbuttonstate">IToolbar::SetButtonState</a>.


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

