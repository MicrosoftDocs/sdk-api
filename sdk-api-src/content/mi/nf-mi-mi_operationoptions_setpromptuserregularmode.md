---
UID: NF:mi.MI_OperationOptions_SetPromptUserRegularMode
title: MI_OperationOptions_SetPromptUserRegularMode function (mi.h)
author: windows-sdk-content
description: Sets the value that tells the server how to respond to a provider's call to the MI_Context_PromptUser function.
old-location: wmi_v2\mi_operationoptions_setpromptuserregularmode.htm
tech.root: wmi_v2
ms.assetid: 4383a407-716a-49d5-b877-67012c48fc6c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_SetPromptUserRegularMode, MI_OperationOptions_SetPromptUserRegularMode function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetPromptUserRegularMode, wmi_v2.mi_operationoptions_setpromptuserregularmode
ms.topic: function
f1_keywords:
- mi/MI_OperationOptions_SetPromptUserRegularMode
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
topic_type:
- kbSyntax
api_type:
- <TBD>
api_location:
- 
api_name:
- MI_OperationOptions_SetPromptUserRegularMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MI_OperationOptions_SetPromptUserRegularMode function


## -description


Sets the value that tells the server how to respond to a provider's call to 
     the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_promptuser">MI_Context_PromptUser</a> function.


## -parameters




### -param options [in, out]

A <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure containing a set of operation options.


### -param mode [in]

The returned <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_callbackmode">MI_CallbackMode</a> enumeration value: either <b>MI_CALLBACKMODE_REPORT</b> or <b>MI_CALLBACKMODE_INQUIRE</b>.


### -param ackValue [in]

TBD


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



