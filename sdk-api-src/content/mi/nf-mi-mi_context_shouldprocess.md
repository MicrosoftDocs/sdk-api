---
UID: NF:mi.MI_Context_ShouldProcess
title: MI_Context_ShouldProcess function
author: windows-sdk-content
description: Queries the client to determine if an operation should continue.
old-location: wmi_v2\mi_context_shouldprocess.htm
old-project: wmi_v2
ms.assetid: adfa899c-f65a-4aac-b82d-5bc7b776713a
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_Context_ShouldProcess, MI_Context_ShouldProcess function [Windows Management Infrastructure (MI)], mi/MI_Context_ShouldProcess, wmi.mi_shouldprocess, wmi_v2.mi_context_shouldprocess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Context_ShouldProcess
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_ShouldProcess function


## -description


Queries the client to determine if an operation should continue.


## -parameters




### -param context [in]

Request context.


### -param target

A null-terminated string that represents the target of the action that is being processed. The string should be in the user's requested locale (retrieved through the <a href="https://msdn.microsoft.com/7d2271e8-de76-4629-aedc-0ab882ab58eb">MI_Context_GetLocale</a> function).


### -param action

A null-terminated string that represents the action that is being processed. The string should be in the user's requested locale (retrieved through the <a href="https://msdn.microsoft.com/7d2271e8-de76-4629-aedc-0ab882ab58eb">MI_Context_GetLocale</a> function).


### -param flag [out]

Boolean response from client indicating if the provider should continue processing. <b>MI_TRUE</b> indicates that the process should continue. <b>MI_FALSE</b> indicates that processing should stop.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



If the client has an auto-result specified, then the message will be reported, but the function will not wait. If the client is not interested in this function, then the function will return immediately with the default response. Otherwise, the function will not return until after the client has responded.

An example use of this function would be when deleting a file. In such a case, you might specify an <i>action</i> parameter of "deleting file" and a <i>target</i> parameter containing the name of the file to be deleted.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/7d2271e8-de76-4629-aedc-0ab882ab58eb">MI_Context_GetLocale</a>



<a href="https://msdn.microsoft.com/ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0">MI_Context_PromptUser</a>



<a href="https://msdn.microsoft.com/5548b75d-2d71-4ef1-828c-ae8fb5e9c165">MI_Context_ShouldContinue</a>
 

 

