---
UID: NS:mi._MI_ReferenceA
title: MI_ReferenceA (mi.h)
description: Represents an array of pointers to MI_Instance types.
helpviewer_keywords: ["MI_ReferenceA","MI_ReferenceA structure [Windows Management Infrastructure (MI)]","mi/MI_ReferenceA","wmi._mi_referencea","wmi_v2.mi_referencea"]
old-location: wmi_v2\mi_referencea.htm
tech.root: wmi_v2
ms.assetid: a0fde623-a9f0-4b7d-8c7d-2a88745fc8b2
ms.date: 12/05/2018
ms.keywords: MI_ReferenceA, MI_ReferenceA structure [Windows Management Infrastructure (MI)], mi/MI_ReferenceA, wmi._mi_referencea, wmi_v2.mi_referencea
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
req.typenames: MI_ReferenceA
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ReferenceA
 - mi/_MI_ReferenceA
 - MI_ReferenceA
 - mi/MI_ReferenceA
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
 - MI_ReferenceA
---

# MI_ReferenceA structure


## -description

Represents an array of pointers to <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> types.

## -struct-fields

### -field data

Pointer to an array of <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structures.

### -field _MI_Instance

### -field size

The number of items in the array.