---
UID: NF:mi.MI_OperationOptions_SetPromptUserMode
title: MI_OperationOptions_SetPromptUserMode function
author: windows-sdk-content
description: Sets the value that tells the server how to respond to a provider's call to the MI_Context_PromptUser function.
old-location: wmi_v2\mi_operationoptions_setpromptusermode.htm
old-project: wmi_v2
ms.assetid: c0bf739d-4da1-4f68-9af8-18874d16e701
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_CALLBACKMODE_INQUIRE, MI_CALLBACKMODE_REPORT, MI_OperationOptions_SetPromptUserMode, MI_OperationOptions_SetPromptUserMode function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetPromptUserMode, wmi_v2.mi_operationoptions_setpromptusermode
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_OperationOptions_SetPromptUserMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_SetPromptUserMode function


## -description


Sets the value that tells the server how to respond to a provider's call to 
     the <a href="https://msdn.microsoft.com/ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0">MI_Context_PromptUser</a> function.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param mode [in]

One of the following <a href="https://msdn.microsoft.com/742610a4-3276-4bab-877d-8e74c6dc80cd">MI_CallbackMode</a> values.



#### MI_CALLBACKMODE_REPORT (0)

Prompt will be passed back to the client in reporting mode, meaning the client is notified of the prompt but cannot respond to it and the server will automatically confirm the request.



#### MI_CALLBACKMODE_INQUIRE (1)

Provider will block while the client is called back to ask if the operation should continue or not.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0">MI_Context_PromptUser</a>



<a href="https://msdn.microsoft.com/662c602a-b16b-41ec-8c37-c0e5860b502b">MI_OperationOptions_GetForceFlagPromptUserMode</a>



<a href="https://msdn.microsoft.com/611e2798-4ab5-405b-9586-5054fe14cd96">MI_OperationOptions_GetPromptUserMode</a>



<a href="https://msdn.microsoft.com/a2e96052-6373-4000-86ca-6f078d299647">MI_OperationOptions_SetForceFlagPromptUserMode</a>
 

 

