---
UID: NF:mmc.IToolbar.SetButtonState
title: IToolbar::SetButtonState
author: windows-sdk-content
description: Enables a snap-in to set an attribute of a button.
old-location: mmc\itoolbar_setbuttonstate.htm
tech.root: mmc
ms.assetid: aa43fc1b-cc6d-474d-9b92-556924fb98de
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: BUTTONPRESSED, CHECKED, ENABLED, HIDDEN, INDETERMINATE, IToolbar interface [MMC],SetButtonState method, IToolbar.SetButtonState, IToolbar::SetButtonState, SetButtonState, SetButtonState method [MMC], SetButtonState method [MMC],IToolbar interface, _slate_itoolbar_setbuttonstate, mmc.itoolbar_setbuttonstate, mmc/IToolbar::SetButtonState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IToolbar.SetButtonState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToolbar::SetButtonState


## -description


The <b>IToolbar::SetButtonState</b> method enables a snap-in to set an attribute of a button.


## -parameters




### -param idCommand [in]

A unique value that the snap-in has associated with a button using the 
<a href="https://msdn.microsoft.com/768df6d0-c2e5-4099-b4a6-a71e4f7e06d7">InsertButton</a> or 
<a href="https://msdn.microsoft.com/9d37d0bc-d7c3-4d23-8dd4-c5a6c4af15ee">AddButtons</a> method using the 
<a href="https://msdn.microsoft.com/340fed49-3003-4dd6-80c9-6cefc8c5b750">MMCBUTTON</a> structure.


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
<a href="https://msdn.microsoft.com/60ed8f9a-d5ad-4a68-8019-6887104c9b2a">IControlbar::Attach</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

