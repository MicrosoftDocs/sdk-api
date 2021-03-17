---
UID: NF:mi.MI_Filter_Evaluate
title: MI_Filter_Evaluate function (mi.h)
description: The provider calls this function to evaluate an instance against a given filter.
helpviewer_keywords: ["MI_Filter_Evaluate","MI_Filter_Evaluate function [Windows Management Infrastructure (MI)]","mi/MI_Filter_Evaluate","wmi_v2.mi_filter_evaluate"]
old-location: wmi_v2\mi_filter_evaluate.htm
tech.root: wmi_v2
ms.assetid: b826f02d-3764-4f61-996f-42bf01ea44e2
ms.date: 12/05/2018
ms.keywords: MI_Filter_Evaluate, MI_Filter_Evaluate function [Windows Management Infrastructure (MI)], mi/MI_Filter_Evaluate, wmi_v2.mi_filter_evaluate
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Filter_Evaluate
 - mi/MI_Filter_Evaluate
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
 - MI_Filter_Evaluate
---

# MI_Filter_Evaluate function


## -description

The provider calls this function to evaluate an instance against a given filter.

## -parameters

### -param self [in]

This is a pointer to the filter the instance will be evaluated against.

### -param instance [in]

This is a pointer to the instance to evaluate.

### -param result [out]

When the API completes, result indicates whether the instance matched the filter.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

