---
UID: NF:combaseapi.CoGetCurrentLogicalThreadId
title: CoGetCurrentLogicalThreadId function (combaseapi.h)
description: Returns the logical thread identifier of the current physical thread.
helpviewer_keywords: ["CoGetCurrentLogicalThreadId","CoGetCurrentLogicalThreadId function [COM]","_com_CoGetCurrentLogicalThreadId","com.cogetcurrentlogicalthreadid","combaseapi/CoGetCurrentLogicalThreadId"]
old-location: com\cogetcurrentlogicalthreadid.htm
tech.root: com
ms.assetid: eced2f1e-9f2b-476c-bea8-945fb4804a89
ms.date: 12/05/2018
ms.keywords: CoGetCurrentLogicalThreadId, CoGetCurrentLogicalThreadId function [COM], _com_CoGetCurrentLogicalThreadId, com.cogetcurrentlogicalthreadid, combaseapi/CoGetCurrentLogicalThreadId
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoGetCurrentLogicalThreadId
 - combaseapi/CoGetCurrentLogicalThreadId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetCurrentLogicalThreadId
---

# CoGetCurrentLogicalThreadId function


## -description

Returns the logical thread identifier of the current physical thread.

## -parameters

### -param pguid [out]

A pointer to a GUID that contains the logical thread ID on return.

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
The logical thread ID was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid pointer was passed in for the <i>pguid</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failed during the operation of the function.

</td>
</tr>
</table>

## -remarks

This function retrieves the identifier of the current logical thread under which this physical thread is operating. The current physical thread takes on the logical thread identifier of any client thread that makes a COM call into this application. Similarly, the logical thread identifier of the current physical thread is used to denote the causality for outgoing COM calls from this physical thread.

