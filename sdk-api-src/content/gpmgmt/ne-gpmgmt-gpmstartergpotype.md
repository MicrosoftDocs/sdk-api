---
UID: NE:gpmgmt.__MIDL___MIDL_itf_gpmgmt_0000_0030_0002
title: GPMStarterGPOType (gpmgmt.h)
description: The Starter Group Policy object is a system Starter Group Policy object or a custom Starter Group Policy object.
helpviewer_keywords: ["GPMStarterGPOType","GPMStarterGPOType enumeration [GPMC]","gpmc.gpmstartergpotype","gpmgmt/GPMStarterGPOType","gpmgmt/typeCustom","gpmgmt/typeSystem","typeCustom","typeSystem"]
old-location: gpmc\gpmstartergpotype.htm
tech.root: gpmc
ms.assetid: 19b84c06-d8dc-4a25-85f6-cfbe9937f30e
ms.date: 12/05/2018
ms.keywords: GPMStarterGPOType, GPMStarterGPOType enumeration [GPMC], gpmc.gpmstartergpotype, gpmgmt/GPMStarterGPOType, gpmgmt/typeCustom, gpmgmt/typeSystem, typeCustom, typeSystem
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GPMStarterGPOType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_gpmgmt_0000_0030_0002
 - gpmgmt/__MIDL___MIDL_itf_gpmgmt_0000_0030_0002
 - GPMStarterGPOType
 - gpmgmt/GPMStarterGPOType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gpmgmt.h
api_name:
 - GPMStarterGPOType
---

# GPMStarterGPOType enumeration


## -description

<b>GPMStarterGPOType</b> defines if  the Starter Group Policy object is a system  Starter Group Policy object or a custom Starter Group Policy object.

<b>GPMStarterGPOType</b> defines if   the Starter Group Policy object is a system  Starter Group Policy object or a custom Starter Group Policy object.

```cpp
typedef enum {
        typeSystem = 0,
        typeCustom
} GPMStarterGPOType;
```

## -enum-fields

### -field typeSystem:0

A system Starter Group Policy object

### -field typeCustom

A  custom Starter Group Policy object

