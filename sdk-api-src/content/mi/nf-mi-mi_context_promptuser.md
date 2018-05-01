---
UID: NF:mi.MI_Context_PromptUser
title: MI_Context_PromptUser function
author: windows-driver-content
description: Sends a prompt message to the client querying whether to continue the operation or cancel it.
old-location: wmi_v2\mi_context_promptuser.htm
old-project: wmi_v2
ms.assetid: ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_Context_PromptUser, MI_Context_PromptUser function [Windows Management Infrastructure (MI)], mi/MI_Context_PromptUser, wmi.mi_promptuser, wmi_v2.mi_context_promptuser
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	MI_Context_PromptUser
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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

Prompt type as defined by <a href="https://msdn.microsoft.com/183f40ed-214f-4468-8036-7753ae18575b">MI_PromptType</a>. The 
      provider should try to use the locale that the client has specified (retrieved through the 
      <a href="https://msdn.microsoft.com/7d2271e8-de76-4629-aedc-0ab882ab58eb">MI_Context_GetLocale</a> function).


### -param flag [out]

Return value from the client. <b>MI_TRUE</b> indicates that the process should continue. 
      <b>MI_FALSE</b> indicates that the process should stop, and the provider should post some 
      final error to say that the operation was cancelled.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.




## -remarks



If the client has an auto-result specified, then the message will be reported, but the function will not wait. 
     If the client is not interested in this function, then the function will return immediately with the default 
     response. Otherwise, the function will not return until after the client has responded to the prompt.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/7d2271e8-de76-4629-aedc-0ab882ab58eb">MI_Context_GetLocale</a>



<a href="https://msdn.microsoft.com/5548b75d-2d71-4ef1-828c-ae8fb5e9c165">MI_Context_ShouldContinue</a>



<a href="https://msdn.microsoft.com/adfa899c-f65a-4aac-b82d-5bc7b776713a">MI_Context_ShouldProcess</a>



<a href="https://msdn.microsoft.com/183f40ed-214f-4468-8036-7753ae18575b">MI_PromptType</a>
 

 

