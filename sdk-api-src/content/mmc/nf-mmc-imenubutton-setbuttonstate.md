---
UID: NF:mmc.IMenuButton.SetButtonState
title: IMenuButton::SetButtonState
author: windows-sdk-content
description: The IMenuButton::SetButtonState method enables a user to change the state of a menu button.
old-location: mmc\imenubutton_setbuttonstate.htm
old-project: mmc
ms.assetid: 28f4faf7-9fb2-4be0-84b6-e3e8f7450c34
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: ENABLED, HIDDEN, IMenuButton interface [MMC],SetButtonState method, IMenuButton.SetButtonState, IMenuButton::SetButtonState, SetButtonState, SetButtonState method [MMC], SetButtonState method [MMC],IMenuButton interface, _slate_imenubutton_setbuttonstate, mmc.imenubutton_setbuttonstate, mmc/IMenuButton::SetButtonState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IMenuButton.SetButtonState
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMenuButton::SetButtonState


## -description


The <b>IMenuButton::SetButtonState</b> method enables a user to change the state of a menu button.


## -parameters




### -param idCommand [in]

A value that specifies a user-supplied value that uniquely identifies the menu button in which the state is being changed.


### -param nState [in]

A value that specifies the state of the button. This value can be one of the following values taken from the 
<a href="https://msdn.microsoft.com/b08c8905-1a6d-485f-9136-d63efd0e8194">MMC_BUTTON_STATE</a> enumeration:



#### ENABLED

The button accepts user input. A button that does not have this state does not accept user input and appears dimmed.



#### HIDDEN

The button is not visible and cannot receive user input.


### -param bState [in]

A value that specifies whether the state is to be turned on or off. <b>TRUE</b> indicates that the  button state is on; otherwise, set to <b>FALSE</b>.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/51bbd98a-7017-497a-858a-dd63cefc679a">IMenuButton</a>
 

 

