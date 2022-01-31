---
UID: NE:mmcobj._MMC_PROPERTY_ACTION
title: MMC_PROPERTY_ACTION (mmcobj.h)
description: The MMC_PROPERTY_ACTION enumeration specifies the operations that can occur to a property contained in an MMC_SNAPIN_PROPERTY structure.
helpviewer_keywords: ["MMC_PROPACT_CHANGING","MMC_PROPACT_DELETING","MMC_PROPACT_INITIALIZED","MMC_PROPERTY_ACTION","MMC_PROPERTY_ACTION enumeration [MMC]","_slate_mmc_property_action","mmc.mmc_property_action","mmcobj/MMC_PROPACT_CHANGING","mmcobj/MMC_PROPACT_DELETING","mmcobj/MMC_PROPACT_INITIALIZED","mmcobj/MMC_PROPERTY_ACTION"]
old-location: mmc\mmc_property_action.htm
tech.root: mmc
ms.assetid: c380d562-0acb-4c90-9460-6007a8eeb596
ms.date: 12/05/2018
ms.keywords: MMC_PROPACT_CHANGING, MMC_PROPACT_DELETING, MMC_PROPACT_INITIALIZED, MMC_PROPERTY_ACTION, MMC_PROPERTY_ACTION enumeration [MMC], _slate_mmc_property_action, mmc.mmc_property_action, mmcobj/MMC_PROPACT_CHANGING, mmcobj/MMC_PROPACT_DELETING, mmcobj/MMC_PROPACT_INITIALIZED, mmcobj/MMC_PROPERTY_ACTION
req.header: mmcobj.h
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
req.typenames: MMC_PROPERTY_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_PROPERTY_ACTION
 - mmcobj/_MMC_PROPERTY_ACTION
 - MMC_PROPERTY_ACTION
 - mmcobj/MMC_PROPERTY_ACTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmcobj.h
api_name:
 - MMC_PROPERTY_ACTION
---

# MMC_PROPERTY_ACTION enumeration


## -description

The 
<b>MMC_PROPERTY_ACTION</b> enumeration specifies the operations that can occur to a property contained in an 
<a href="/windows/desktop/api/mmcobj/ns-mmcobj-mmc_snapin_property">MMC_SNAPIN_PROPERTY</a> structure.

## -enum-fields

### -field MMC_PROPACT_DELETING:1

The property is being deleted.

### -field MMC_PROPACT_CHANGING

The property is being modified.

### -field MMC_PROPACT_INITIALIZED

The property is being added.

## -see-also

<a href="/windows/desktop/api/mmcobj/nf-mmcobj-isnapinproperties-propertieschanged">ISnapinProperties::PropertiesChanged</a>



<a href="/windows/desktop/api/mmcobj/ns-mmcobj-mmc_snapin_property">MMC_SNAPIN_PROPERTY</a>
