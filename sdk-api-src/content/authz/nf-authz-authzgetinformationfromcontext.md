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

# AuthzGetInformationFromContext function


## -description


The <b>AuthzGetInformationFromContext</b> function returns information about an Authz context. 

Starting with Windows Server 2012 and Windows 8, device groups are returned as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure. User and device claims are returned as an <a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure.


## -parameters




### -param hAuthzClientContext [in]

A handle to the context.


### -param InfoClass [in]

A value of the <a href="https://msdn.microsoft.com/5eb752dc-17f7-4510-8aef-d18280322e76">AUTHZ_CONTEXT_INFORMATION_CLASS</a> enumeration that indicates the type of information to be returned.


### -param BufferSize [in]

Size of the buffer passed.


### -param pSizeRequired [out]

A pointer to a <b>DWORD</b> of  the buffer size required for returning the structure.


### -param Buffer [out]

A pointer to memory that can receive the information. The structure returned depends on the information requested in the <i>InfoClass</i> parameter.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/5eb752dc-17f7-4510-8aef-d18280322e76">AUTHZ_CONTEXT_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a>
 

 

