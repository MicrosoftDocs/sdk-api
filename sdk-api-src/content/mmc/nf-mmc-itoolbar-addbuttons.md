---
UID: NF:mmc.IToolbar.AddButtons
title: IToolbar::AddButtons (mmc.h)
description: Enables a snap-in to add an array of buttons to the toolbar.
helpviewer_keywords: ["AddButtons","AddButtons method [MMC]","AddButtons method [MMC]","IToolbar interface","IToolbar interface [MMC]","AddButtons method","IToolbar.AddButtons","IToolbar::AddButtons","_slate_itoolbar_addbuttons","mmc.itoolbar_addbuttons","mmc/IToolbar::AddButtons"]
old-location: mmc\itoolbar_addbuttons.htm
tech.root: mmc
ms.assetid: 9d37d0bc-d7c3-4d23-8dd4-c5a6c4af15ee
ms.date: 12/05/2018
ms.keywords: AddButtons, AddButtons method [MMC], AddButtons method [MMC],IToolbar interface, IToolbar interface [MMC],AddButtons method, IToolbar.AddButtons, IToolbar::AddButtons, _slate_itoolbar_addbuttons, mmc.itoolbar_addbuttons, mmc/IToolbar::AddButtons
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
 - IToolbar::AddButtons
 - mmc/IToolbar::AddButtons
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
 - IToolbar.AddButtons
---

# IToolbar::AddButtons


## -description

The <b>IToolbar::AddButtons</b> method enables a snap-in to add an array of buttons to the toolbar.

## -parameters

### -param nButtons [in]

The number of buttons in the array.

### -param lpButtons [in]

A pointer to the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmcbutton">MMCBUTTON</a> structure that contains information necessary for creating a button on the toolbar.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>