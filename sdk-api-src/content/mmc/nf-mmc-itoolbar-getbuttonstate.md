---
UID: NF:mmc.IToolbar.GetButtonState
title: IToolbar::GetButtonState (mmc.h)
description: Enables a snap-in to obtain an attribute of a button.
helpviewer_keywords: ["BUTTONPRESSED","CHECKED","ENABLED","GetButtonState","GetButtonState method [MMC]","GetButtonState method [MMC]","IToolbar interface","HIDDEN","INDETERMINATE","IToolbar interface [MMC]","GetButtonState method","IToolbar.GetButtonState","IToolbar::GetButtonState","_slate_itoolbar_getbuttonstate","mmc.itoolbar_getbuttonstate","mmc/IToolbar::GetButtonState"]
old-location: mmc\itoolbar_getbuttonstate.htm
tech.root: mmc
ms.assetid: 94c41b13-f1ab-4368-8cfa-960caeea796e
ms.date: 12/05/2018
ms.keywords: BUTTONPRESSED, CHECKED, ENABLED, GetButtonState, GetButtonState method [MMC], GetButtonState method [MMC],IToolbar interface, HIDDEN, INDETERMINATE, IToolbar interface [MMC],GetButtonState method, IToolbar.GetButtonState, IToolbar::GetButtonState, _slate_itoolbar_getbuttonstate, mmc.itoolbar_getbuttonstate, mmc/IToolbar::GetButtonState
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
 - IToolbar::GetButtonState
 - mmc/IToolbar::GetButtonState
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
 - IToolbar.GetButtonState
---

# IToolbar::GetButtonState


## -description

The <b>IToolbar::GetButtonState</b> method enables a snap-in to obtain an attribute of a button.

## -parameters

### -param idCommand [in]

The command identifier of the toolbar button.

### -param nState [in]

A value that identifies the possible states of the button. Can be one of the following:



#### ENABLED

The button accepts user input. A button that does not have this state does not accept user input and appears dimmed.



#### CHECKED

The button has the CHECKED style and is being pressed.



#### HIDDEN

The button is not visible and cannot receive user input.



#### INDETERMINATE

The button appears dimmed.



#### BUTTONPRESSED

The button is being pressed.

### -param pState [out]

A pointer to the state information that is returned.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>