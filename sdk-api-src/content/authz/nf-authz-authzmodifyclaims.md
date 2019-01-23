---
UID: NF:authz.AuthzModifyClaims
title: AuthzModifyClaims function
author: windows-sdk-content
description: Adds, deletes, or modifies user and device claims in the Authz client context.
old-location: security\authzmodifyclaims.htm
tech.root: SecAuthZ
ms.assetid: A93CD1DD-4E87-4C6A-928A-F90AD7F1085E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AuthzModifyClaims, AuthzModifyClaims function [Security], authz/AuthzModifyClaims, security.authzmodifyclaims
ms.topic: function
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzModifyClaims
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



