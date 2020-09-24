---
UID: NF:mmc.IToolbar.SetButtonState
title: IToolbar::SetButtonState (mmc.h)
description: Enables a snap-in to set an attribute of a button.
helpviewer_keywords: ["BUTTONPRESSED","CHECKED","ENABLED","HIDDEN","INDETERMINATE","IToolbar interface [MMC]","SetButtonState method","IToolbar.SetButtonState","IToolbar::SetButtonState","SetButtonState","SetButtonState method [MMC]","SetButtonState method [MMC]","IToolbar interface","_slate_itoolbar_setbuttonstate","mmc.itoolbar_setbuttonstate","mmc/IToolbar::SetButtonState"]
old-location: mmc\itoolbar_setbuttonstate.htm
tech.root: mmc
ms.assetid: aa43fc1b-cc6d-474d-9b92-556924fb98de
ms.date: 12/05/2018
ms.keywords: BUTTONPRESSED, CHECKED, ENABLED, HIDDEN, INDETERMINATE, IToolbar interface [MMC],SetButtonState method, IToolbar.SetButtonState, IToolbar::SetButtonState, SetButtonState, SetButtonState method [MMC], SetButtonState method [MMC],IToolbar interface, _slate_itoolbar_setbuttonstate, mmc.itoolbar_setbuttonstate, mmc/IToolbar::SetButtonState
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
 - IToolbar::SetButtonState
 - mmc/IToolbar::SetButtonState
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
 - IToolbar.SetButtonState
---

# IToolbar::SetButtonState


## -description

The <b>IToolbar::SetButtonState</b> method enables a snap-in to set an attribute of a button.

## -parameters

### -param idCommand [in]

A unique value that the snap-in has associated with a button using the 
<a href="/windows/desktop/api/mmc/nf-mmc-itoolbar-insertbutton">InsertButton</a> or 
<a href="/windows/desktop/api/mmc/nf-mmc-itoolbar-addbuttons">AddButtons</a> method using the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmcbutton">MMCBUTTON</a> structure.

### -param nState [in]

A value that specifies the state to be set for the button. Can be any one of the following:



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

### -param bState [in]

A value that specifies whether the state identified in nState is set to <b>TRUE</b> or <b>FALSE</b>. <b>TRUE</b> sets the button state to the state identified by nState and <b>FALSE</b> clears the state (if it is already set).

## -returns

This method can return one of these values.

## -remarks

Snap-ins should not set button states until the toolbar has been attached using 
<a href="/windows/desktop/api/mmc/nf-mmc-icontrolbar-attach">IControlbar::Attach</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>