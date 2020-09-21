---
UID: NF:mi.MI_Context_SetStringOption
title: MI_Context_SetStringOption function (mi.h)
description: Sets a context-specific option.
helpviewer_keywords: ["MI_Context_SetStringOption","MI_Context_SetStringOption function [Windows Management Infrastructure (MI)]","mi/MI_Context_SetStringOption","wmi.mi_setstringoption","wmi_v2.mi_context_setstringoption"]
old-location: wmi_v2\mi_context_setstringoption.htm
tech.root: wmi_v2
ms.assetid: a7affdbe-1fc7-4662-8f21-077138365adf
ms.date: 12/05/2018
ms.keywords: MI_Context_SetStringOption, MI_Context_SetStringOption function [Windows Management Infrastructure (MI)], mi/MI_Context_SetStringOption, wmi.mi_setstringoption, wmi_v2.mi_context_setstringoption
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
 - MI_Context_SetStringOption
 - mi/MI_Context_SetStringOption
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
 - MI_Context_SetStringOption
---

# MI_Context_SetStringOption function


## -description

Sets a context-specific option.

## -parameters

### -param context [in]

Request context.

### -param name

A null-terminated string that represents the name of the option to change.

### -param value

A null-terminated string that represents the new value for the specified option.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

This function allows the provider to adjust the server's behavior.

On Windows Server 2012, this function only supports the "SECURITY" option, which is used only by an indication provider to control which users have permission to subscribe to the indication class. The function is valid if and only if it is called inside the indication class's *_Load function.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getcustomoption">MI_Context_GetCustomOption</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getcustomoptionat">MI_Context_GetCustomOptionAt</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getcustomoptioncount">MI_Context_GetCustomOptionCount</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getnumberoption">MI_Context_GetNumberOption</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getstringoption">MI_Context_GetStringOption</a>