---
UID: NF:mmc.IMenuButton.SetButtonState
title: IMenuButton::SetButtonState (mmc.h)
description: The IMenuButton::SetButtonState method enables a user to change the state of a menu button.
helpviewer_keywords: ["ENABLED","HIDDEN","IMenuButton interface [MMC]","SetButtonState method","IMenuButton.SetButtonState","IMenuButton::SetButtonState","SetButtonState","SetButtonState method [MMC]","SetButtonState method [MMC]","IMenuButton interface","_slate_imenubutton_setbuttonstate","mmc.imenubutton_setbuttonstate","mmc/IMenuButton::SetButtonState"]
old-location: mmc\imenubutton_setbuttonstate.htm
tech.root: mmc
ms.assetid: 28f4faf7-9fb2-4be0-84b6-e3e8f7450c34
ms.date: 12/05/2018
ms.keywords: ENABLED, HIDDEN, IMenuButton interface [MMC],SetButtonState method, IMenuButton.SetButtonState, IMenuButton::SetButtonState, SetButtonState, SetButtonState method [MMC], SetButtonState method [MMC],IMenuButton interface, _slate_imenubutton_setbuttonstate, mmc.imenubutton_setbuttonstate, mmc/IMenuButton::SetButtonState
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
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMenuButton::SetButtonState
 - mmc/IMenuButton::SetButtonState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IMenuButton.SetButtonState
---

# IMenuButton::SetButtonState


## -description

The <b>IMenuButton::SetButtonState</b> method enables a user to change the state of a menu button.

## -parameters

### -param idCommand [in]

A value that specifies a user-supplied value that uniquely identifies the menu button in which the state is being changed.

### -param nState [in]

A value that specifies the state of the button. This value can be one of the following values taken from the 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_button_state">MMC_BUTTON_STATE</a> enumeration:



#### ENABLED

The button accepts user input. A button that does not have this state does not accept user input and appears dimmed.



#### HIDDEN

The button is not visible and cannot receive user input.

### -param bState [in]

A value that specifies whether the state is to be turned on or off. <b>TRUE</b> indicates that the  button state is on; otherwise, set to <b>FALSE</b>.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-imenubutton">IMenuButton</a>