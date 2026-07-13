---
UID: NF:mi.MI_OperationOptions_GetPromptUserMode
title: MI_OperationOptions_GetPromptUserMode function (mi.h)
description: Gets the value that tells the server how to respond to a provider's call to MI_Context_PromptUser. (MI_OperationOptions_GetPromptUserMode)
helpviewer_keywords: ["MI_OperationOptions_GetPromptUserMode","MI_OperationOptions_GetPromptUserMode function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_GetPromptUserMode","wmi_v2.mi_operationoptions_getpromptusermode"]
old-location: wmi_v2\mi_operationoptions_getpromptusermode.htm
tech.root: wmi_v2
ms.assetid: 611e2798-4ab5-405b-9586-5054fe14cd96
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetPromptUserMode, MI_OperationOptions_GetPromptUserMode function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetPromptUserMode, wmi_v2.mi_operationoptions_getpromptusermode
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
 - MI_OperationOptions_GetPromptUserMode
 - mi/MI_OperationOptions_GetPromptUserMode
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
 - MI_OperationOptions_GetPromptUserMode
---

# MI_OperationOptions_GetPromptUserMode function


## -description

Gets the value that tells the server how to respond to a provider's call to 
     <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_promptuser">MI_Context_PromptUser</a>.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param mode [out]

The returned <a href="/windows/desktop/api/mi/ne-mi-mi_callbackmode">MI_CallbackMode</a> enumeration value: either MI_CALLBACKMODE_REPORT or MI_CALLBACKMODE_INQUIRE.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ne-mi-mi_callbackmode">MI_CallbackMode</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_promptuser">MI_Context_PromptUser</a>



<a href="/previous-versions/windows/desktop/legacy/hh449233(v=vs.85)">MI_OperationOptions_GetForceFlagPromptUserMode</a>



<a href="/previous-versions/windows/desktop/legacy/hh449249(v=vs.85)">MI_OperationOptions_SetForceFlagPromptUserMode</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_setpromptusermode">MI_OperationOptions_SetPromptUserMode</a>
