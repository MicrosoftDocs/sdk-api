---
UID: NF:combaseapi.CoGetCallContext
title: CoGetCallContext function (combaseapi.h)
description: Retrieves the context of the current call on the current thread.
helpviewer_keywords: ["CoGetCallContext","CoGetCallContext function [COM]","_com_CoGetCallContext","com.cogetcallcontext","combaseapi/CoGetCallContext"]
old-location: com\cogetcallcontext.htm
tech.root: com
ms.assetid: b82e32c0-840d-402e-90d5-ff678c51faf1
ms.date: 12/05/2018
ms.keywords: CoGetCallContext, CoGetCallContext function [COM], _com_CoGetCallContext, com.cogetcallcontext, combaseapi/CoGetCallContext
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - CoGetCallContext
 - combaseapi/CoGetCallContext
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
 - CoGetCallContext
---

# CoGetCallContext function


## -description

Retrieves the context of the current call on the current thread.

## -parameters

### -param riid [in]

Interface identifier (IID) of the call context that is being requested. If you are using the default call context supported by standard marshaling, IID_IServerSecurity is available. For COM+ applications using role-based security, IID_ISecurityCallContext is available.

### -param ppInterface [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppInterface</i> contains the requested interface pointer.

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
The context was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The call context does not support the interface specified by <i>riid</i>.

</td>
</tr>
</table>

## -remarks

<b>CoGetCallContext</b> retrieves the context of the current call on the current thread. The <i>riid</i> parameter specifies the interface on the context to be retrieved. This is one of the functions provided to give the server access to any contextual information of the caller.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a>



<a href="/windows/desktop/com/security-in-com">Security in COM</a>