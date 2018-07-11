---
UID: NS:mmcobj._MMC_SNAPIN_PROPERTY
title: "_MMC_SNAPIN_PROPERTY"
author: windows-sdk-content
description: The MMC_SNAPIN_PROPERTY structure is introduced in MMC 2.0.
old-location: mmc\mmc_snapin_property.htm
old-project: mmc
ms.assetid: 0815d6a0-ddc2-43d1-aafd-5a05352557fc
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: MMC_SNAPIN_PROPERTY, MMC_SNAPIN_PROPERTY structure [MMC], _MMC_SNAPIN_PROPERTY, _slate_mmc_snapin_property, mmc.mmc_snapin_property, mmcobj/MMC_SNAPIN_PROPERTY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MMC_SNAPIN_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmcobj.h
api_name:
 - MMC_SNAPIN_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MMC_SNAPIN_PROPERTY structure


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
<a href="https://msdn.microsoft.com/c380d562-0acb-4c90-9460-6007a8eeb596">MMC_PROPERTY_ACTION</a>.


## -see-also




<a href="https://msdn.microsoft.com/6e64a620-9c1d-4803-81a0-ec432c30fbc9">ISnapinProperties::PropertiesChanged</a>



<a href="https://msdn.microsoft.com/c380d562-0acb-4c90-9460-6007a8eeb596">MMC_PROPERTY_ACTION</a>
 

 

