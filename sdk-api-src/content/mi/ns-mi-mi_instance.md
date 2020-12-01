---
UID: NS:mi._MI_Instance
title: MI_Instance (mi.h)
description: This structure represents a CIM instance. This object should not be accessed directly. Instead, the MI_Instance_* functions should be used.
helpviewer_keywords: ["MI_Instance","MI_Instance structure [Windows Management Infrastructure (MI)]","mi/MI_Instance","wmi._mi_instance","wmi_v2.mi_instance"]
old-location: wmi_v2\mi_instance.htm
tech.root: wmi_v2
ms.assetid: 3dce1817-7995-49e5-8cc0-ee9496665e5c
ms.date: 12/05/2018
ms.keywords: MI_Instance, MI_Instance structure [Windows Management Infrastructure (MI)], mi/MI_Instance, wmi._mi_instance, wmi_v2.mi_instance
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
req.typenames: MI_Instance
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,   Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_Instance
 - mi/_MI_Instance
 - MI_Instance
 - mi/MI_Instance
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
 - MI_Instance
---

# MI_Instance structure


## -description

This structure represents a CIM instance. This object should not be accessed directly. Instead, the 
  <b>MI_Instance_*</b> functions should be used.

## -struct-fields

### -field ft

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_instanceft">MI_InstanceFT</a> function table.

### -field classDecl

The class declaration for this instance.

### -field serverName

Optional server name. Can be null.

### -field nameSpace

Optional namespace. Can be null.

### -field reserved

Reserved for internal use.