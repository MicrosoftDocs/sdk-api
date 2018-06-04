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

# AuthzModifySecurityAttributes function


## -description


The <b>AuthzModifySecurityAttributes</b> function modifies the security attribute information in the specified client context.


## -parameters




### -param hAuthzClientContext [in]

A handle to the client context to be modified.


### -param pOperations [in]

A pointer to an array of <a href="https://msdn.microsoft.com/c1716cdb-87f9-47d6-bfc3-ae6cc043e917">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a> enumeration values that specify the types of modifications to make.

This array must have only one element if the value of that element is <b>AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE_ALL</b>. Otherwise, the array has the same number of elements as the <i>pAttributes</i> array.


### -param pAttributes [in]

A pointer to an <a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that specifies the attributes to modify.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



