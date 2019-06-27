---
UID: NF:mi.MI_OperationOptions_SetPromptUserMode
title: MI_OperationOptions_SetPromptUserMode function (mi.h)
author: windows-sdk-content
description: Sets the value that tells the server how to respond to a provider's call to the MI_Context_PromptUser function.
old-location: wmi_v2\mi_operationoptions_setpromptusermode.htm
tech.root: wmi_v2
ms.assetid: c0bf739d-4da1-4f68-9af8-18874d16e701
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_CALLBACKMODE_INQUIRE, MI_CALLBACKMODE_REPORT, MI_OperationOptions_SetPromptUserMode, MI_OperationOptions_SetPromptUserMode function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetPromptUserMode, wmi_v2.mi_operationoptions_setpromptusermode
ms.topic: function
f1_keywords: 
 - "mi/MI_OperationOptions_SetPromptUserMode"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationOptions_SetPromptUserMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_OperationOptions_SetPromptUserMode function


## -description


Sets the value that tells the server how to respond to a provider's call to 
     the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_promptuser">MI_Context_PromptUser</a> function.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/ns-mi-_mi_operationoptions">MI_OperationOptions</a> structure.


### -param mode [in]

One of the following <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/ne-mi-_mi_callbackmode">MI_CallbackMode</a> values.



#### MI_CALLBACKMODE_REPORT (0)

Prompt will be passed back to the client in reporting mode, meaning the client is notified of the prompt but cannot respond to it and the server will automatically confirm the request.



#### MI_CALLBACKMODE_INQUIRE (1)

Provider will block while the client is called back to ask if the operation should continue or not.


## -returns



A value of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/ne-mi-_mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_promptuser">MI_Context_PromptUser</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449233(v=vs.85)">MI_OperationOptions_GetForceFlagPromptUserMode</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getpromptusermode">MI_OperationOptions_GetPromptUserMode</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449249(v=vs.85)">MI_OperationOptions_SetForceFlagPromptUserMode</a>
 

 

