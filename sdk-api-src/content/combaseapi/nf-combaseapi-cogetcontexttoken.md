---
UID: NF:combaseapi.CoGetContextToken
title: CoGetContextToken function (combaseapi.h)
description: Returns a pointer to an implementation of IObjContext for the current context.
helpviewer_keywords: ["CoGetContextToken","CoGetContextToken function [COM]","_com_CoGetContextToken","com.cogetcontexttoken","combaseapi/CoGetContextToken"]
old-location: com\cogetcontexttoken.htm
tech.root: com
ms.assetid: 1218d928-ca3f-4bdc-9a00-ea4c214175a9
ms.date: 12/05/2018
ms.keywords: CoGetContextToken, CoGetContextToken function [COM], _com_CoGetContextToken, com.cogetcontexttoken, combaseapi/CoGetContextToken
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
 - CoGetContextToken
 - combaseapi/CoGetContextToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetContextToken
---

# CoGetContextToken function


## -description

Returns a pointer to an implementation of <a href="/windows/desktop/api/objidl/nn-objidl-iobjcontext">IObjContext</a> for the current context.

## -parameters

### -param pToken [out]

A pointer to an implementation of <a href="/windows/desktop/api/objidl/nn-objidl-iobjcontext">IObjContext</a> for the current context.

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

<a href="/windows/desktop/api/objidl/nn-objidl-icontext">IContext</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iobjcontext">IObjContext</a>