---
UID: NF:mmc.IExtendControlbar.SetControlbar
title: IExtendControlbar::SetControlbar (mmc.h)
description: The IExtendControlbar::SetControlbar method attaches or detaches a control bar.
helpviewer_keywords: ["IExtendControlbar interface [MMC]","SetControlbar method","IExtendControlbar.SetControlbar","IExtendControlbar::SetControlbar","SetControlbar","SetControlbar method [MMC]","SetControlbar method [MMC]","IExtendControlbar interface","_slate_iextendcontrolbar_setcontrolbar","mmc.iextendcontrolbar_setcontrolbar","mmc/IExtendControlbar::SetControlbar"]
old-location: mmc\iextendcontrolbar_setcontrolbar.htm
tech.root: mmc
ms.assetid: 5088eff2-b7a0-4c16-a33c-3a82bc2e72af
ms.date: 12/05/2018
ms.keywords: IExtendControlbar interface [MMC],SetControlbar method, IExtendControlbar.SetControlbar, IExtendControlbar::SetControlbar, SetControlbar, SetControlbar method [MMC], SetControlbar method [MMC],IExtendControlbar interface, _slate_iextendcontrolbar_setcontrolbar, mmc.iextendcontrolbar_setcontrolbar, mmc/IExtendControlbar::SetControlbar
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtendControlbar::SetControlbar
 - mmc/IExtendControlbar::SetControlbar
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendControlbar.SetControlbar
---

# IExtendControlbar::SetControlbar


## -description

The <b>IExtendControlbar::SetControlbar</b> method attaches or detaches a control bar.

## -parameters

### -param pControlbar [in]

A pointer to an 
<a href="/windows/desktop/api/mmc/nn-mmc-icontrolbar">IControlbar</a> interface on the control bar object to be set. A non-<b>NULL</b> value attaches a control bar; a <b>NULL</b> value detaches a control bar.

## -returns

This method can return one of these values.

## -remarks

As items are selected and deselected, snap-ins are activated and deactivated. When a snap-in is activated, the console calls 
SetControlbar with a non-<b>NULL</b> pControlbar value. The snap-in should call AddRef on this IControlBar. The snap-in should also use this opportunity to attach controls. Similarly, when the snap-in is deactivated, the console calls 
SetControlbar with a <b>NULL</b> pControlbar. The snap-in should then detach its controls and call Release on the saved IControlBar.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>