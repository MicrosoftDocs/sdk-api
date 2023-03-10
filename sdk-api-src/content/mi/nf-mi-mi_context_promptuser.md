---
UID: NF:mi.MI_Context_PromptUser
title: MI_Context_PromptUser function (mi.h)
description: Sends a prompt message to the client querying whether to continue the operation or cancel it.
helpviewer_keywords: ["MI_Context_PromptUser","MI_Context_PromptUser function [Windows Management Infrastructure (MI)]","mi/MI_Context_PromptUser","wmi.mi_promptuser","wmi_v2.mi_context_promptuser"]
old-location: wmi_v2\mi_context_promptuser.htm
tech.root: wmi_v2
ms.assetid: ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0
ms.date: 12/05/2018
ms.keywords: MI_Context_PromptUser, MI_Context_PromptUser function [Windows Management Infrastructure (MI)], mi/MI_Context_PromptUser, wmi.mi_promptuser, wmi_v2.mi_context_promptuser
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
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Context_PromptUser
 - mi/MI_Context_PromptUser
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
 - MI_Context_PromptUser
---

# MI_Context_PromptUser function


## -description

Sends a prompt message to the client querying whether to continue the operation or cancel it.

## -parameters

### -param context [in]

Request context.

### -param message [in]

A null-terminated string that represents the prompt message for the client.

### -param promptType

Prompt type as defined by <a href="/windows/desktop/api/mi/ne-mi-mi_prompttype">MI_PromptType</a>. The 
      provider should try to use the locale that the client has specified (retrieved through the 
      <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getlocale">MI_Context_GetLocale</a> function).

### -param flag [out]

Return value from the client. <b>MI_TRUE</b> indicates that the process should continue. 
      <b>MI_FALSE</b> indicates that the process should stop, and the provider should post some 
      final error to say that the operation was cancelled.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.

## -remarks

If the client has an auto-result specified, then the message will be reported, but the function will not wait. 
     If the client is not interested in this function, then the function will return immediately with the default 
     response. Otherwise, the function will not return until after the client has responded to the prompt.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getlocale">MI_Context_GetLocale</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_shouldcontinue">MI_Context_ShouldContinue</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_shouldprocess">MI_Context_ShouldProcess</a>



<a href="/windows/desktop/api/mi/ne-mi-mi_prompttype">MI_PromptType</a>