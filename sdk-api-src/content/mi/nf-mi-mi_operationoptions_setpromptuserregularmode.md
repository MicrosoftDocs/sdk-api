---
UID: NF:mi.MI_OperationOptions_SetPromptUserRegularMode
title: MI_OperationOptions_SetPromptUserRegularMode function
author: windows-sdk-content
description: Sets the value that tells the server how to respond to a provider's call to the MI_Context_PromptUser function.
old-location: wmi_v2\mi_operationoptions_setpromptuserregularmode.htm
tech.root: wmi_v2
ms.assetid: 4383a407-716a-49d5-b877-67012c48fc6c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_OperationOptions_SetPromptUserRegularMode, MI_OperationOptions_SetPromptUserRegularMode function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetPromptUserRegularMode, wmi_v2.mi_operationoptions_setpromptuserregularmode
ms.topic: function
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
 - HeaderDef
api_location:
 -
api_name:
 - MI_OperationOptions_SetPromptUserRegularMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MI_OperationOptions_SetPromptUserRegularMode function


## -description


Sets the value that tells the server how to respond to a provider's call to 
     the <a href="https://msdn.microsoft.com/ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0">MI_Context_PromptUser</a> function.


## -parameters




### -param options [in, out]

A <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure containing a set of operation options.


### -param mode [in]

The returned <a href="https://msdn.microsoft.com/742610a4-3276-4bab-877d-8e74c6dc80cd">MI_CallbackMode</a> enumeration value: either <b>MI_CALLBACKMODE_REPORT</b> or <b>MI_CALLBACKMODE_INQUIRE</b>.


### -param ackValue [in]

TBD


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



