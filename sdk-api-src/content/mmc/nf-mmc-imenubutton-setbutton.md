---
UID: NF:mmc.IMenuButton.SetButton
title: IMenuButton::SetButton (mmc.h)
description: The IMenuButton::SetButton method enables a user to set the text attributes of a button in the menu bar that is changed.
helpviewer_keywords: ["IMenuButton interface [MMC]","SetButton method","IMenuButton.SetButton","IMenuButton::SetButton","SetButton","SetButton method [MMC]","SetButton method [MMC]","IMenuButton interface","_slate_imenubutton_setbutton","mmc.imenubutton_setbutton","mmc/IMenuButton::SetButton"]
old-location: mmc\imenubutton_setbutton.htm
tech.root: mmc
ms.assetid: f0297c54-7aa2-497b-9fe7-1be4fc7517f9
ms.date: 12/05/2018
ms.keywords: IMenuButton interface [MMC],SetButton method, IMenuButton.SetButton, IMenuButton::SetButton, SetButton, SetButton method [MMC], SetButton method [MMC],IMenuButton interface, _slate_imenubutton_setbutton, mmc.imenubutton_setbutton, mmc/IMenuButton::SetButton
f1_keywords:
- mmc/IMenuButton.SetButton
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
- IMenuButton.SetButton
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMenuButton::SetButton


## -description


The <b>IMenuButton::SetButton</b> method enables a user to set the text attributes of a button in the menu bar that is changed.


## -parameters




### -param idCommand [in]

A value that specifies a user-supplied value that uniquely identifies the button to be added to the menu bar.


### -param lpButtonText [in]

A pointer to the text value (a null-terminated string) to be displayed on the button.


### -param lpTooltipText [in]

A pointer to the text value (a null-terminated string) to be displayed when the user places the mouse pointer on the button.


## -returns



This method can return one of these values.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-imenubutton">IMenuButton</a>
 

 

