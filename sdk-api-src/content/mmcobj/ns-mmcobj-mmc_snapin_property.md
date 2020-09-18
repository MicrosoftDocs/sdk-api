---
UID: NS:mmcobj._MMC_SNAPIN_PROPERTY
title: MMC_SNAPIN_PROPERTY (mmcobj.h)
description: The MMC_SNAPIN_PROPERTY structure is introduced in MMC 2.0.
helpviewer_keywords: ["MMC_SNAPIN_PROPERTY","MMC_SNAPIN_PROPERTY structure [MMC]","_slate_mmc_snapin_property","mmc.mmc_snapin_property","mmcobj/MMC_SNAPIN_PROPERTY"]
old-location: mmc\mmc_snapin_property.htm
tech.root: mmc
ms.assetid: 0815d6a0-ddc2-43d1-aafd-5a05352557fc
ms.date: 12/05/2018
ms.keywords: MMC_SNAPIN_PROPERTY, MMC_SNAPIN_PROPERTY structure [MMC], _slate_mmc_snapin_property, mmc.mmc_snapin_property, mmcobj/MMC_SNAPIN_PROPERTY
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
req.typenames: MMC_SNAPIN_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_SNAPIN_PROPERTY
 - mmcobj/_MMC_SNAPIN_PROPERTY
 - MMC_SNAPIN_PROPERTY
 - mmcobj/MMC_SNAPIN_PROPERTY
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
 - MMC_SNAPIN_PROPERTY
---

# MMC_SNAPIN_PROPERTY structure


## -description

The 
<b>MMC_SNAPIN_PROPERTY</b> structure is introduced in MMC 2.0.

The 
<b>MMC_SNAPIN_PROPERTY</b> structure is used by a snap-in when a property is added, changed, or deleted.

## -struct-fields

### -field pszPropName

Name of the property.

### -field varValue

The property's value; if the property is being changed, this is the new value.

### -field eAction

The action taking place on the property, as defined in 
<a href="/windows/desktop/api/mmcobj/ne-mmcobj-mmc_property_action">MMC_PROPERTY_ACTION</a>.

## -see-also

<a href="/windows/desktop/api/mmcobj/nf-mmcobj-isnapinproperties-propertieschanged">ISnapinProperties::PropertiesChanged</a>



<a href="/windows/desktop/api/mmcobj/ne-mmcobj-mmc_property_action">MMC_PROPERTY_ACTION</a>