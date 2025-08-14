---
UID: NF:combaseapi.CoGetObjectContext
title: CoGetObjectContext function (combaseapi.h)
description: Returns the context for the current object.
helpviewer_keywords: ["CoGetObjectContext","CoGetObjectContext function [COM]","_com_CoGetObjectContext","com.cogetobjectcontext","combaseapi/CoGetObjectContext"]
old-location: com\cogetobjectcontext.htm
tech.root: com
ms.assetid: 97a0c6c3-a011-44dc-b428-aabdad7d4364
ms.date: 12/05/2018
ms.keywords: CoGetObjectContext, CoGetObjectContext function [COM], _com_CoGetObjectContext, com.cogetobjectcontext, combaseapi/CoGetObjectContext
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
 - CoGetObjectContext
 - combaseapi/CoGetObjectContext
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
 - CoGetObjectContext
---

# CoGetObjectContext function


## -description

Returns the context for the current object.

## -parameters

### -param riid [in]

A reference to the ID of an interface that is implemented on the context object. 

For objects running within COM applications, IID_IComThreadingInfo, IID_IContext, and IID_IContextCallback are available.

For objects running within COM+ applications, IID_IObjectContext, IID_IObjectContextActivity IID_IObjectContextInfo, and IID_IContextState are available.

### -param ppv [out]

The address of a pointer to the interface specified by <i>riid</i> on the context object.

## -returns

This function can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The object context was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface was not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
Before this function can be called, the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> function must be called on the current thread.

</td>
</tr>
</table>

## -remarks

<b>CoGetObjectContext</b> retrieves the context for the object from which it is called, and returns a pointer to an interface that can be used to manipulate context properties. Context properties are used to provide services to configured components running within COM+ applications.

For components running within COM applications, the following interfaces are supported for accessing context properties: <a href="/windows/desktop/api/objidl/nn-objidl-icomthreadinginfo">IComThreadingInfo</a>, <a href="/windows/desktop/api/objidl/nn-objidl-icontext">IContext</a>, and <a href="/windows/desktop/api/ctxtcall/nn-ctxtcall-icontextcallback">IContextCallback</a>.

For components running within COM+ applications, the following interfaces are supported for accessing context properties: <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>, <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextactivity">IObjectContextActivity</a>, <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a>, and <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextstate">IContextState</a>.

## -see-also

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">Contexts and Threading Models</a>