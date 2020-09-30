---
UID: NS:mmc._MENUBUTTONDATA
title: MENUBUTTONDATA (mmc.h)
description: The MENUBUTTONDATA structure contains values used to create buttons on a toolbar.
helpviewer_keywords: ["*LPMENUBUTTONDATA","LPMENUBUTTONDATA","LPMENUBUTTONDATA structure pointer [MMC]","MENUBUTTONDATA","MENUBUTTONDATA structure [MMC]","_slate_menubuttondata","mmc.menubuttondata","mmc/LPMENUBUTTONDATA","mmc/MENUBUTTONDATA"]
old-location: mmc\menubuttondata.htm
tech.root: mmc
ms.assetid: 440467ea-3d6c-49a0-a81a-24088e307d22
ms.date: 12/05/2018
ms.keywords: '*LPMENUBUTTONDATA, LPMENUBUTTONDATA, LPMENUBUTTONDATA structure pointer [MMC], MENUBUTTONDATA, MENUBUTTONDATA structure [MMC], _slate_menubuttondata, mmc.menubuttondata, mmc/LPMENUBUTTONDATA, mmc/MENUBUTTONDATA'
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
req.typenames: MENUBUTTONDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MENUBUTTONDATA
 - mmc/_MENUBUTTONDATA
 - MENUBUTTONDATA
 - mmc/MENUBUTTONDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MENUBUTTONDATA
---

# MENUBUTTONDATA structure


## -description

The 
<b>MENUBUTTONDATA</b> structure contains values used to create buttons on a toolbar.

## -struct-fields

### -field idCommand

A value that specifies a user-supplied value that uniquely identifies the menu button.

### -field x

A value that specifies the horizontal position, in pixels, at which the snap-in's context menu is displayed.

### -field y

A value that specifies the vertical position, in pixels, at which the snap-in's context menu is displayed.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-imenubutton">IMenuButton</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-menu-btnclick">MMCN_MENU_BTNCLICK</a>