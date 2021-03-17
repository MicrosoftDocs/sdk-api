---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt
title: MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt function (mi.h)
description: Gets a previously added credential password based on a specified index.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt","MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt","wmi_v2.mi_subscriptiondeliveryoptions_getcredentialspasswordat"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getcredentialspasswordat.htm
tech.root: wmi_v2
ms.assetid: 338fba5a-160e-4744-84c5-28aa1f115f53
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt, MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt, wmi_v2.mi_subscriptiondeliveryoptions_getcredentialspasswordat
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt
 - mi/MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt
---

# MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt function


## -description

Gets a previously added credential password based on a specified index.

## -parameters

### -param self [in]

A <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param index

Zero-based index of the credential password.

### -param optionName

A pointer to a null-terminated string containing the returned name of the option. This name is owned by the <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param password

Returned password. This parameter is an in/out buffer that is passed in to be filled. This buffer should be cleared (using the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function) as soon as the password is no longer needed for security reasons. If the input value is <b>NULL</b>, the <i>bufferLength</i> parameter should be zero, and the length needed will be passed back in the <i>passwordLength</i> parameter.

### -param bufferLength [in]

Length of the password buffer. If 0, the <b>passwordLength</b> value will receive the length of the buffer needed.

### -param passwordLength [out]

Returned password length.

### -param flags [out, optional]

Returned credential flags.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>