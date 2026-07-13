---
UID: NF:mi.MI_Context_ShouldContinue
title: MI_Context_ShouldContinue function (mi.h)
description: Queries the client to determine if an operation should continue. (MI_Context_ShouldContinue)
helpviewer_keywords: ["MI_Context_ShouldContinue","MI_Context_ShouldContinue function [Windows Management Infrastructure (MI)]","mi/MI_Context_ShouldContinue","wmi.mi_shouldcontinue","wmi_v2.mi_context_shouldcontinue"]
old-location: wmi_v2\mi_context_shouldcontinue.htm
tech.root: wmi_v2
ms.assetid: 5548b75d-2d71-4ef1-828c-ae8fb5e9c165
ms.date: 12/05/2018
ms.keywords: MI_Context_ShouldContinue, MI_Context_ShouldContinue function [Windows Management Infrastructure (MI)], mi/MI_Context_ShouldContinue, wmi.mi_shouldcontinue, wmi_v2.mi_context_shouldcontinue
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
 - MI_Context_ShouldContinue
 - mi/MI_Context_ShouldContinue
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
 - MI_Context_ShouldContinue
---

# MI_Context_ShouldContinue function


## -description

Queries the client to determine if an operation should continue.

## -parameters

### -param context [in]

Request context.

### -param message

A null-terminated string that represents the message prompt that the client displays to the user. The message should be in the user's requested locale (retrieved through the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getlocale">MI_Context_GetLocale</a> function).

### -param flag [out]

Boolean response from client indicating if the provider should continue processing. <b>MI_TRUE</b> indicates that the process should continue. <b>MI_FALSE</b> indicates that processing should stop.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

If the client has an auto-result specified, then the message will be reported, but the function will not wait. If the client is not interested in this function, then the function will return immediately with the default response. Otherwise, the function will not return until after the client has responded.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getlocale">MI_Context_GetLocale</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_promptuser">MI_Context_PromptUser</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_shouldprocess">MI_Context_ShouldProcess</a>
