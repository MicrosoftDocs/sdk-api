---
UID: NF:mmc.IToolbar.InsertButton
title: IToolbar::InsertButton (mmc.h)
description: Enables a snap-in to add a single button to the toolbar.
helpviewer_keywords: ["IToolbar interface [MMC]","InsertButton method","IToolbar.InsertButton","IToolbar::InsertButton","InsertButton","InsertButton method [MMC]","InsertButton method [MMC]","IToolbar interface","_slate_itoolbar_insertbutton","mmc.itoolbar_insertbutton","mmc/IToolbar::InsertButton"]
old-location: mmc\itoolbar_insertbutton.htm
tech.root: mmc
ms.assetid: 768df6d0-c2e5-4099-b4a6-a71e4f7e06d7
ms.date: 12/05/2018
ms.keywords: IToolbar interface [MMC],InsertButton method, IToolbar.InsertButton, IToolbar::InsertButton, InsertButton, InsertButton method [MMC], InsertButton method [MMC],IToolbar interface, _slate_itoolbar_insertbutton, mmc.itoolbar_insertbutton, mmc/IToolbar::InsertButton
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
 - IToolbar::InsertButton
 - mmc/IToolbar::InsertButton
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
 - IToolbar.InsertButton
---

# IToolbar::InsertButton


## -description

The <b>IToolbar::InsertButton</b> method enables a snap-in to add a single button to the toolbar. The button being added is placed at the end of the toolbar.

## -parameters

### -param nIndex [in]

An internal index at which the button will be inserted. The button is always placed at the end of the toolbar; the internal index is required if the button is to be deleted (by means of 
<a href="/windows/desktop/api/mmc/nf-mmc-itoolbar-deletebutton">IToolbar::DeleteButton</a>).

### -param lpButton [in]

A pointer to the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmcbutton">MMCBUTTON</a> structure that defines the button to be inserted.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>