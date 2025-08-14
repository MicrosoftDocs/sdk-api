---
UID: NF:combaseapi.CoGetCancelObject
title: CoGetCancelObject function (combaseapi.h)
description: Obtains a pointer to a call control interface, normally ICancelMethodCalls, on the cancel object corresponding to an outbound COM method call pending on the same or another client thread.
helpviewer_keywords: ["CoGetCancelObject","CoGetCancelObject function [COM]","_com_CoGetCancelObject","com.cogetcancelobject","combaseapi/CoGetCancelObject"]
old-location: com\cogetcancelobject.htm
tech.root: com
ms.assetid: d38161af-d662-4430-99b7-6563efda6f4e
ms.date: 12/05/2018
ms.keywords: CoGetCancelObject, CoGetCancelObject function [COM], _com_CoGetCancelObject, com.cogetcancelobject, combaseapi/CoGetCancelObject
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
 - CoGetCancelObject
 - combaseapi/CoGetCancelObject
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
 - CoGetCancelObject
---

# CoGetCancelObject function


## -description

Obtains a pointer to a call control interface, normally <a href="/windows/desktop/api/objidl/nn-objidl-icancelmethodcalls">ICancelMethodCalls</a>, on the cancel object corresponding to an outbound COM method call pending on the same or another client thread.

## -parameters

### -param dwThreadId [in]

The identifier of the thread on which the pending COM call is to be canceled. If this parameter is 0, the call is on the current thread.

### -param iid [in]

The globally unique identifier of an interface on the cancel object for the call to be canceled. This argument is usually IID_ICancelMethodCalls.

### -param ppUnk [out]

Receives the address of a pointer to the interface specified by <i>riid</i>.

## -returns

This function can return the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The call control object was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object on which the call is executing does not support the interface specified by <i>riid</i>.

</td>
</tr>
</table>

## -remarks

If two or more calls are pending on the same thread through nested calls, the thread ID may not be sufficient to identify the call to be canceled. In this case, <b>CoGetCancelObject</b> returns a cancel interface corresponding to the innermost call that is pending on the thread and has registered a cancel object.

This function does not locate cancel objects for asynchronous calls.