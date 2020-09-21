---
UID: NF:mi.MI_Context_GetCustomOptionCount
title: MI_Context_GetCustomOptionCount function (mi.h)
description: Gets the number of custom options available to the provider.
helpviewer_keywords: ["MI_Context_GetCustomOptionCount","MI_Context_GetCustomOptionCount function [Windows Management Infrastructure (MI)]","mi/MI_Context_GetCustomOptionCount","wmi.mi_getcustomoptioncount","wmi_v2.mi_context_getcustomoptioncount"]
old-location: wmi_v2\mi_context_getcustomoptioncount.htm
tech.root: wmi_v2
ms.assetid: 8cce1492-5c3a-4ba8-8f33-22f6ff7fcf3a
ms.date: 12/05/2018
ms.keywords: MI_Context_GetCustomOptionCount, MI_Context_GetCustomOptionCount function [Windows Management Infrastructure (MI)], mi/MI_Context_GetCustomOptionCount, wmi.mi_getcustomoptioncount, wmi_v2.mi_context_getcustomoptioncount
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
 - MI_Context_GetCustomOptionCount
 - mi/MI_Context_GetCustomOptionCount
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
 - MI_Context_GetCustomOptionCount
---

# MI_Context_GetCustomOptionCount function


## -description

Gets the number of custom options available to the provider.

## -parameters

### -param context [in]

A pointer to the request context.

### -param count [out, optional]

A pointer to the returned number of options. This parameter is optional.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

These options are passed by the client, possibly through the <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a>