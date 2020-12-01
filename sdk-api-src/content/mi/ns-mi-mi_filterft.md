---
UID: NS:mi._MI_FilterFT
title: MI_FilterFT (mi.h)
description: A support structure used in the MI_Filter structure. Use the functions with the name prefix &quot;MI_Filter_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_FilterFT","MI_FilterFT structure [Windows Management Infrastructure (MI)]","mi/MI_FilterFT","wmi_v2.mi_filterft"]
old-location: wmi_v2\mi_filterft.htm
tech.root: wmi_v2
ms.assetid: f090b05e-e99b-47aa-8458-8e2cf9031ac7
ms.date: 12/05/2018
ms.keywords: MI_FilterFT, MI_FilterFT structure [Windows Management Infrastructure (MI)], mi/MI_FilterFT, wmi_v2.mi_filterft
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
req.typenames: MI_FilterFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_FilterFT
 - mi/_MI_FilterFT
 - MI_FilterFT
 - mi/MI_FilterFT
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
 - MI_FilterFT
---

## -description

A support structure used in the <a href="/windows/desktop/api/mi/ns-mi-mi_filter">MI_Filter</a> 
    structure. Use the functions with the name prefix "MI_Filter_" to manipulate these 
    structures.

## -struct-fields

### -field Evaluate

The provider calls this function to evaluate an instance against a given filter. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_filter_evaluate">MI_Filter_Evaluate</a>.

### -field GetExpression

Gets the filter language and expression. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_filter_getexpression">MI_Filter_GetExpression</a>.
