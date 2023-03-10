---
UID: NF:mmcobj.ISnapinProperties.PropertiesChanged
title: ISnapinProperties::PropertiesChanged (mmcobj.h)
description: Called when a property is added, changed, or deleted.
helpviewer_keywords: ["ISnapinProperties interface [MMC]","PropertiesChanged method","ISnapinProperties.PropertiesChanged","ISnapinProperties::PropertiesChanged","PropertiesChanged","PropertiesChanged method [MMC]","PropertiesChanged method [MMC]","ISnapinProperties interface","_slate_isnapinproperties_propertieschanged","mmc.isnapinproperties_propertieschanged","mmcobj/ISnapinProperties::PropertiesChanged"]
old-location: mmc\isnapinproperties_propertieschanged.htm
tech.root: mmc
ms.assetid: 6e64a620-9c1d-4803-81a0-ec432c30fbc9
ms.date: 12/05/2018
ms.keywords: ISnapinProperties interface [MMC],PropertiesChanged method, ISnapinProperties.PropertiesChanged, ISnapinProperties::PropertiesChanged, PropertiesChanged, PropertiesChanged method [MMC], PropertiesChanged method [MMC],ISnapinProperties interface, _slate_isnapinproperties_propertieschanged, mmc.isnapinproperties_propertieschanged, mmcobj/ISnapinProperties::PropertiesChanged
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISnapinProperties::PropertiesChanged
 - mmcobj/ISnapinProperties::PropertiesChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcobj.h
api_name:
 - ISnapinProperties.PropertiesChanged
---

# ISnapinProperties::PropertiesChanged


## -description

The 
<b>PropertiesChanged</b> method is called when a property is added, changed, or deleted. A snap-in can reject the change or deletion by returning E_FAIL.

## -parameters

### -param cProperties [in]

The number of 
<a href="/windows/desktop/api/mmcobj/ns-mmcobj-mmc_snapin_property">MMC_SNAPIN_PROPERTY</a> structures provided by <i>pProperties</i>.

### -param pProperties [in]

An array of 
<a href="/windows/desktop/api/mmcobj/ns-mmcobj-mmc_snapin_property">MMC_SNAPIN_PROPERTY</a> structures.

## -returns

If successful, the return value is <b>S_OK</b>; a snap-in can prevent a change or deletion from occurring by returning <b>E_FAIL</b>.

## -see-also

<a href="/windows/desktop/api/mmcobj/ne-mmcobj-mmc_property_action">MMC_PROPERTY_ACTION</a>



<a href="/windows/desktop/api/mmcobj/ns-mmcobj-mmc_snapin_property">MMC_SNAPIN_PROPERTY</a>