---
UID: NF:mmc.IMenuButton.AddButton
title: IMenuButton::AddButton (mmc.h)
description: The IMenuButton::AddButton method enables a user to add a button to the MMC menu bar for a particular view.
helpviewer_keywords: ["AddButton","AddButton method [MMC]","AddButton method [MMC]","IMenuButton interface","IMenuButton interface [MMC]","AddButton method","IMenuButton.AddButton","IMenuButton::AddButton","_slate_imenubutton_addbutton","mmc.imenubutton_addbutton","mmc/IMenuButton::AddButton"]
old-location: mmc\imenubutton_addbutton.htm
tech.root: mmc
ms.assetid: 75d19e2a-0d3e-4883-852e-983fcee8166a
ms.date: 12/05/2018
ms.keywords: AddButton, AddButton method [MMC], AddButton method [MMC],IMenuButton interface, IMenuButton interface [MMC],AddButton method, IMenuButton.AddButton, IMenuButton::AddButton, _slate_imenubutton_addbutton, mmc.imenubutton_addbutton, mmc/IMenuButton::AddButton
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
 - IMenuButton::AddButton
 - mmc/IMenuButton::AddButton
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
 - IMenuButton.AddButton
---

# IMenuButton::AddButton


## -description

The <b>IMenuButton::AddButton</b> method enables a user to add a button to the MMC menu bar for a particular view.

## -parameters

### -param idCommand [in]

A value that specifies a user-supplied value that uniquely identifies the button to be added to the menu bar.

### -param lpButtonText [in]

A pointer to the text value (a null-terminated string) to be displayed on the button.

### -param lpTooltipText [in]

A pointer to the text value (a null-terminated string) to be displayed when the user places the mouse pointer on the button.

## -returns

This method can return one of these values.

## -remarks

Buttons added to the MMC menu bar for a particular view are always appended to the buttons already present. The initial state of any menu button is hidden and disabled.

When the snap-in loses the focus, these buttons are automatically removed from the menu bar. As a result, they must be added each time the snap-in gets the focus.

This method can be called by primary or extension snap-ins.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-imenubutton">IMenuButton</a>