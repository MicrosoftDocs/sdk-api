---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt
title: MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt function (mi.h)
author: windows-sdk-content
description: Gets a previously added credential password based on a specified index.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getcredentialspasswordat.htm
tech.root: wmi_v2
ms.assetid: 338fba5a-160e-4744-84c5-28aa1f115f53
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt, MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt, wmi_v2.mi_subscriptiondeliveryoptions_getcredentialspasswordat
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
 - MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
 

 

