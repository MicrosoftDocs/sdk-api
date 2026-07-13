---
UID: NF:mi.MI_OperationOptions_GetPromptUserRegularMode
title: MI_OperationOptions_GetPromptUserRegularMode function (mi.h)
description: Gets the value that tells the server how to respond to a provider's call to MI_Context_PromptUser. (MI_OperationOptions_GetPromptUserRegularMode)
helpviewer_keywords: ["MI_OperationOptions_GetPromptUserRegularMode","MI_OperationOptions_GetPromptUserRegularMode function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_GetPromptUserRegularMode","wmi_v2.mi_operationoptions_getpromptuserregularmode"]
old-location: wmi_v2\mi_operationoptions_getpromptuserregularmode.htm
tech.root: wmi_v2
ms.assetid: 10c22de2-3f07-4d91-aa95-c59285d6087f
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetPromptUserRegularMode, MI_OperationOptions_GetPromptUserRegularMode function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetPromptUserRegularMode, wmi_v2.mi_operationoptions_getpromptuserregularmode
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
req.lib: Mi.lib
req.dll: Mi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MI_OperationOptions_GetPromptUserRegularMode
 - mi/MI_OperationOptions_GetPromptUserRegularMode
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - MI_OperationOptions_GetPromptUserRegularMode
---

# MI_OperationOptions_GetPromptUserRegularMode function


## -description

Gets the value that tells the server how to respond to a provider's call to 
     <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_promptuser">MI_Context_PromptUser</a>.

## -parameters

### -param options [in, out]

A <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure containing a set of operation options.

### -param mode [out]

The returned <a href="/windows/desktop/api/mi/ne-mi-mi_callbackmode">MI_CallbackMode</a> enumeration value: either <b>MI_CALLBACKMODE_REPORT</b> or <b>MI_CALLBACKMODE_INQUIRE</b>.

### -param ackValue [out]

TBD

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.
