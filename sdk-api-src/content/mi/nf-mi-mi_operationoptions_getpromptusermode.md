---
UID: NF:mi.MI_OperationOptions_GetPromptUserMode
title: MI_OperationOptions_GetPromptUserMode function (mi.h)
author: windows-sdk-content
description: Gets the value that tells the server how to respond to a provider's call to MI_Context_PromptUser.
old-location: wmi_v2\mi_operationoptions_getpromptusermode.htm
tech.root: wmi_v2
ms.assetid: 611e2798-4ab5-405b-9586-5054fe14cd96
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetPromptUserMode, MI_OperationOptions_GetPromptUserMode function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetPromptUserMode, wmi_v2.mi_operationoptions_getpromptusermode
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
 - MI_OperationOptions_GetPromptUserMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_OperationOptions_GetPromptUserMode function


## -description


Gets the value that tells the server how to respond to a provider's call to 
     <a href="https://msdn.microsoft.com/ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0">MI_Context_PromptUser</a>.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param mode [out]

The returned <a href="https://msdn.microsoft.com/742610a4-3276-4bab-877d-8e74c6dc80cd">MI_CallbackMode</a> enumeration value: either MI_CALLBACKMODE_REPORT or MI_CALLBACKMODE_INQUIRE.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/742610a4-3276-4bab-877d-8e74c6dc80cd">MI_CallbackMode</a>



<a href="https://msdn.microsoft.com/ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0">MI_Context_PromptUser</a>



<a href="https://msdn.microsoft.com/662c602a-b16b-41ec-8c37-c0e5860b502b">MI_OperationOptions_GetForceFlagPromptUserMode</a>



<a href="https://msdn.microsoft.com/a2e96052-6373-4000-86ca-6f078d299647">MI_OperationOptions_SetForceFlagPromptUserMode</a>



<a href="https://msdn.microsoft.com/c0bf739d-4da1-4f68-9af8-18874d16e701">MI_OperationOptions_SetPromptUserMode</a>
 

 

