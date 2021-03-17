---
UID: NS:mi._MI_Server
title: MI_Server (mi.h)
description: This structure defines default function tables for all types:\_Context, Instance, PropertySet, and Filter.
helpviewer_keywords: ["MI_Server","MI_Server structure [Windows Management Infrastructure (MI)]","mi/MI_Server","wmi._mi_server","wmi_v2.mi_server"]
old-location: wmi_v2\mi_server.htm
tech.root: wmi_v2
ms.assetid: bbe367c4-1964-4f6d-9345-fa19c090e018
ms.date: 12/05/2018
ms.keywords: MI_Server, MI_Server structure [Windows Management Infrastructure (MI)], mi/MI_Server, wmi._mi_server, wmi_v2.mi_server
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
req.typenames: MI_Server
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_Server
 - mi/_MI_Server
 - MI_Server
 - mi/MI_Server
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
 - MI_Server
---

# MI_Server structure


## -description

This structure defines default function tables
 for all types: Context, Instance, PropertySet, and Filter.

## -struct-fields

### -field serverFT

Pointer to an <b>MI_Server</b> function table.

### -field contextFT

Pointer to <a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a> function table.

### -field instanceFT

Pointer to <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> function table.

### -field propertySetFT

Pointer to <a href="/windows/desktop/api/mi/ns-mi-mi_propertyset">MI_PropertySet</a> function table.

### -field filterFT

Pointer to <a href="/windows/desktop/api/mi/ns-mi-mi_filter">MI_Filter</a> function table.