---
UID: NF:mmc.IControlbar.Attach
title: IControlbar::Attach (mmc.h)
description: The IControlbar::Attach method allows the snap-in to associate a control with a control bar.
helpviewer_keywords: ["Attach","Attach method [MMC]","Attach method [MMC]","IControlbar interface","IControlbar interface [MMC]","Attach method","IControlbar.Attach","IControlbar::Attach","_slate_icontrolbar_attach","mmc.icontrolbar_attach","mmc/IControlbar::Attach"]
old-location: mmc\icontrolbar_attach.htm
tech.root: mmc
ms.assetid: 60ed8f9a-d5ad-4a68-8019-6887104c9b2a
ms.date: 12/05/2018
ms.keywords: Attach, Attach method [MMC], Attach method [MMC],IControlbar interface, IControlbar interface [MMC],Attach method, IControlbar.Attach, IControlbar::Attach, _slate_icontrolbar_attach, mmc.icontrolbar_attach, mmc/IControlbar::Attach
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
 - IControlbar::Attach
 - mmc/IControlbar::Attach
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
 - IControlbar.Attach
---

# IControlbar::Attach


## -description

The <b>IControlbar::Attach</b> method allows the snap-in to associate a control with a control bar.

## -parameters

### -param nType [in]

A value that specifies the type of control to be associated with the control bar, taken from the 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_control_type">MMC_CONTROL_TYPE</a> enumeration.

### -param lpUnknown [in]

A pointer to the IUnknown interface on the control object to be inserted.

## -returns

This method can return one of these values.

## -remarks

Although COMBOBOXBAR appears in Mmc.idl in connection with the nType parameter, it is not implemented.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>