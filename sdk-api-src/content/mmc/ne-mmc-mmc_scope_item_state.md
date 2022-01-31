---
UID: NE:mmc._MMC_SCOPE_ITEM_STATE
title: MMC_SCOPE_ITEM_STATE (mmc.h)
description: Used to specify the nState member of the SCOPEDATAITEM structure.
helpviewer_keywords: ["MMC_SCOPE_ITEM_STATE","MMC_SCOPE_ITEM_STATE enumeration [MMC]","MMC_SCOPE_ITEM_STATE_BOLD","MMC_SCOPE_ITEM_STATE_EXPANDEDONCE","MMC_SCOPE_ITEM_STATE_NORMAL","_slate_mmc_scope_item_state","mmc.mmc_scope_item_state","mmc/MMC_SCOPE_ITEM_STATE","mmc/MMC_SCOPE_ITEM_STATE_BOLD","mmc/MMC_SCOPE_ITEM_STATE_EXPANDEDONCE","mmc/MMC_SCOPE_ITEM_STATE_NORMAL"]
old-location: mmc\mmc_scope_item_state.htm
tech.root: mmc
ms.assetid: 6c1755a4-ea6e-4c0e-a84e-f609aca0085c
ms.date: 12/05/2018
ms.keywords: MMC_SCOPE_ITEM_STATE, MMC_SCOPE_ITEM_STATE enumeration [MMC], MMC_SCOPE_ITEM_STATE_BOLD, MMC_SCOPE_ITEM_STATE_EXPANDEDONCE, MMC_SCOPE_ITEM_STATE_NORMAL, _slate_mmc_scope_item_state, mmc.mmc_scope_item_state, mmc/MMC_SCOPE_ITEM_STATE, mmc/MMC_SCOPE_ITEM_STATE_BOLD, mmc/MMC_SCOPE_ITEM_STATE_EXPANDEDONCE, mmc/MMC_SCOPE_ITEM_STATE_NORMAL
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
req.typenames: MMC_SCOPE_ITEM_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_SCOPE_ITEM_STATE
 - mmc/_MMC_SCOPE_ITEM_STATE
 - MMC_SCOPE_ITEM_STATE
 - mmc/MMC_SCOPE_ITEM_STATE
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
 - MMC_SCOPE_ITEM_STATE
---

# MMC_SCOPE_ITEM_STATE enumeration


## -description

The 
MMC_SCOPE_ITEM_STATE enumeration is used to specify the <b>nState</b> member of the 
<a href="/windows/desktop/api/mmc/ns-mmc-scopedataitem">SCOPEDATAITEM</a> structure.

## -enum-fields

### -field MMC_SCOPE_ITEM_STATE_NORMAL:0x1

Not currently used.

### -field MMC_SCOPE_ITEM_STATE_BOLD:0x2

Not currently used.

### -field MMC_SCOPE_ITEM_STATE_EXPANDEDONCE:0x3

Set if the item has been expanded at least once or 0 (zero) if the item has not been expanded.
