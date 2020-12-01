---
UID: NS:cloneviewhelper.tagAdapters
title: Adapters (cloneviewhelper.h)
description: The Adapters structure contains a list of graphics adapters.
helpviewer_keywords: ["Adapters","Adapters structure [Display Devices]","TMM_Ref_5b0d959d-9d91-4166-8555-633b0690de8a.xml","cloneviewhelper/Adapters","display.adapters"]
old-location: display\adapters.htm
tech.root: display
ms.assetid: 4f91e683-66f6-4667-86d0-d3de28ba64b0
ms.date: 12/05/2018
ms.keywords: Adapters, Adapters structure [Display Devices], TMM_Ref_5b0d959d-9d91-4166-8555-633b0690de8a.xml, cloneviewhelper/Adapters, display.adapters
req.header: cloneviewhelper.h
req.include-header: Cloneviewhelper.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr: 
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
req.typenames: Adapters
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAdapters
 - cloneviewhelper/tagAdapters
 - Adapters
 - cloneviewhelper/Adapters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cloneviewhelper.h
api_name:
 - Adapters
---

# Adapters structure


## -description

The Adapters structure contains a list of graphics adapters.

## -struct-fields

### -field numAdapters

The number of graphics adapters in the array that the <b>adapter</b> member specifies.

### -field adapter

An array of <a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-adapter">Adapter</a> structures that specify information about graphics adapters.

## -see-also

<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-adapter">Adapter</a>



<a href="/previous-versions/windows/hardware/drivers/ff568176(v=vs.85)">IViewHelper::SetConfiguration</a>