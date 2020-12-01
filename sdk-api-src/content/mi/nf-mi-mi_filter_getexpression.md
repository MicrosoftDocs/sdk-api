---
UID: NF:mi.MI_Filter_GetExpression
title: MI_Filter_GetExpression function (mi.h)
description: Gets the filter language and expression.
helpviewer_keywords: ["MI_Filter_GetExpression","MI_Filter_GetExpression function [Windows Management Infrastructure (MI)]","mi/MI_Filter_GetExpression","wmi_v2.mi_filter_getexpression"]
old-location: wmi_v2\mi_filter_getexpression.htm
tech.root: wmi_v2
ms.assetid: a1ba9cf2-b613-4621-a4ac-39808b4bfd8e
ms.date: 12/05/2018
ms.keywords: MI_Filter_GetExpression, MI_Filter_GetExpression function [Windows Management Infrastructure (MI)], mi/MI_Filter_GetExpression, wmi_v2.mi_filter_getexpression
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
 - MI_Filter_GetExpression
 - mi/MI_Filter_GetExpression
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
 - MI_Filter_GetExpression
---

# MI_Filter_GetExpression function


## -description

Gets the filter language and expression.

## -parameters

### -param self [in]

Pointer to the filter

### -param queryLang

Returned query string.

### -param queryExpr

Returned query expression.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

