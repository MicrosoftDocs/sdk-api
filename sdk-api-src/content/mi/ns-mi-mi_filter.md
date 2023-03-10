---
UID: NS:mi._MI_Filter
title: MI_Filter (mi.h)
description: Contains a reference to the function table MI_FilterFT.
helpviewer_keywords: ["MI_Filter","MI_Filter structure [Windows Management Infrastructure (MI)]","mi/MI_Filter","wmi._mi_filter","wmi_v2.mi_filter"]
old-location: wmi_v2\mi_filter.htm
tech.root: wmi_v2
ms.assetid: 0849cb55-ba2f-4855-ac33-fa96d8ecd94f
ms.date: 12/05/2018
ms.keywords: MI_Filter, MI_Filter structure [Windows Management Infrastructure (MI)], mi/MI_Filter, wmi._mi_filter, wmi_v2.mi_filter
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
req.typenames: MI_Filter
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_Filter
 - mi/_MI_Filter
 - MI_Filter
 - mi/MI_Filter
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
 - MI_Filter
---

# MI_Filter structure


## -description

Contains a reference to the function table <a href="/windows/desktop/api/mi/ns-mi-mi_filterft">MI_FilterFT</a>.

## -struct-fields

### -field ft

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_filterft">MI_FilterFT</a> function table.

### -field reserved

Reserved for internal use.