---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

