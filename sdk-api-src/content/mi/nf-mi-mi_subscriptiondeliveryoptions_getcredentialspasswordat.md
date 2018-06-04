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

# MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt function


## -description


Gets a previously added credential password based on a specified index.


## -parameters




### -param self [in]

A <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param index

Zero-based index of the credential password.


### -param optionName

A pointer to a null-terminated string containing the returned name of the option. This name is owned by the <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param password

Returned password. This parameter is an in/out buffer that is passed in to be filled. This buffer should be cleared (using the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function) as soon as the password is no longer needed for security reasons. If the input value is <b>NULL</b>, the <i>bufferLength</i> parameter should be zero, and the length needed will be passed back in the <i>passwordLength</i> parameter.


### -param bufferLength [in]

Length of the password buffer. If 0, the <b>passwordLength</b> value will receive the length of the buffer needed.


### -param passwordLength [out]

Returned password length.


### -param flags [out, optional]

Returned credential flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>
 

 

