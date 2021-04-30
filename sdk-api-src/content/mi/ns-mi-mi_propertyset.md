---
UID: NS:mi._MI_PropertySet
title: MI_PropertySet (mi.h)
description: Implements a set of property names.
helpviewer_keywords: ["MI_PropertySet","MI_PropertySet structure [Windows Management Infrastructure (MI)]","mi/MI_PropertySet","wmi._mi_propertyset","wmi_v2.mi_propertyset"]
old-location: wmi_v2\mi_propertyset.htm
tech.root: wmi_v2
ms.assetid: 7c9e41b0-818e-46aa-8900-5006904f78d5
ms.date: 12/05/2018
ms.keywords: MI_PropertySet, MI_PropertySet structure [Windows Management Infrastructure (MI)], mi/MI_PropertySet, wmi._mi_propertyset, wmi_v2.mi_propertyset
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_PropertySet
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_PropertySet
 - mi/_MI_PropertySet
 - MI_PropertySet
 - mi/MI_PropertySet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_PropertySet
---

# MI_PropertySet structure


## -description

Implements a set of property names.

## -struct-fields

### -field ft

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_propertysetft">MI_PropertySetFT</a> function table.

### -field reserved

Reserved for internal use.

## -remarks

It supports the building and interrogation of property sets. In general, clients  build property sets and providers interrogate them.