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

# AuthzModifyClaims function


## -description


The <b>AuthzModifyClaims</b> function adds, deletes, or modifies user and device claims in the Authz client context.


## -parameters




### -param hAuthzClientContext [in]

A handle to the client context to be modified.


### -param ClaimClass [in]

Type of information to be modified. The caller can specify AuthzContextInfoUserClaims or AuthzContextInfoDeviceClaims.


### -param pClaimOperations [in]

A pointer to an array of <a href="https://msdn.microsoft.com/c1716cdb-87f9-47d6-bfc3-ae6cc043e917">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a> enumeration values that specify the type of claim modification to make.


### -param pClaims [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that specifies the claims to modify.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <a href="https://msdn.microsoft.com/c1716cdb-87f9-47d6-bfc3-ae6cc043e917">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a> enumeration must have only one element if 
    the value of that element is AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE_ALL. 
    Otherwise, the array has the same number of elements as the corresponding 
    PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION.


If the <a href="https://msdn.microsoft.com/c1716cdb-87f9-47d6-bfc3-ae6cc043e917">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a> enumeration is AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE and the function fails, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the error code is ERROR_ALREADY_EXISTS, the claim's values have duplicate entries.



