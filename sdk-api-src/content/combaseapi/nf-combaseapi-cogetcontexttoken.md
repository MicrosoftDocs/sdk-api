---
UID: NF:combaseapi.CoGetContextToken
title: CoGetContextToken function
author: windows-sdk-content
description: Returns a pointer to an implementation of IObjContext for the current context.
old-location: com\cogetcontexttoken.htm
tech.root: com
ms.assetid: 1218d928-ca3f-4bdc-9a00-ea4c214175a9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CoGetContextToken, CoGetContextToken function [COM], _com_CoGetContextToken, com.cogetcontexttoken, combaseapi/CoGetContextToken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetContextToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoGetContextToken function


## -description


Returns a pointer to an implementation of <a href="https://msdn.microsoft.com/983615a1-cfa2-4137-8c7e-42e2ef6923a8">IObjContext</a> for the current context.




## -parameters




### -param pToken [out]

A pointer to an implementation of <a href="https://msdn.microsoft.com/983615a1-cfa2-4137-8c7e-42e2ef6923a8">IObjContext</a> for the current context.


## -returns



This function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The token was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The caller did not pass a valid token pointer variable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The caller is not in an initialized apartment.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/89c41d9c-186c-4927-990d-92aa501f7d35">IContext</a>



<a href="https://msdn.microsoft.com/983615a1-cfa2-4137-8c7e-42e2ef6923a8">IObjContext</a>
 

 

