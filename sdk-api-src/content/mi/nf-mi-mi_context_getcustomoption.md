---
UID: NF:mi.MI_Context_GetCustomOption
title: MI_Context_GetCustomOption function (mi.h)
description: Retrieves an option set by the client.
helpviewer_keywords: ["MI_Context_GetCustomOption","MI_Context_GetCustomOption function [Windows Management Infrastructure (MI)]","mi/MI_Context_GetCustomOption","wmi.mi_getcustomoption","wmi_v2.mi_context_getcustomoption"]
old-location: wmi_v2\mi_context_getcustomoption.htm
tech.root: wmi_v2
ms.assetid: 3338ca5c-48ac-450f-bf2a-ded6a2c3da19
ms.date: 12/05/2018
ms.keywords: MI_Context_GetCustomOption, MI_Context_GetCustomOption function [Windows Management Infrastructure (MI)], mi/MI_Context_GetCustomOption, wmi.mi_getcustomoption, wmi_v2.mi_context_getcustomoption
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
 - MI_Context_GetCustomOption
 - mi/MI_Context_GetCustomOption
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
 - MI_Context_GetCustomOption
---

# MI_Context_GetCustomOption function


## -description

Retrieves an option set by the client.

## -parameters

### -param context [in]

A pointer to the request context.

### -param name

A pointer to the name of the option to get.

### -param valueType [out, optional]

A pointer to the option value type. This parameter is optional.

### -param value [out, optional]

A pointer to the option value. This parameter is optional.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.