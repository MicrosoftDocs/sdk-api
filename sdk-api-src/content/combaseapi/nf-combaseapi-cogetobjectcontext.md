---
UID: NF:combaseapi.CoGetObjectContext
title: CoGetObjectContext function
author: windows-sdk-content
description: Returns the context for the current object.
old-location: com\cogetobjectcontext.htm
tech.root: com
ms.assetid: 97a0c6c3-a011-44dc-b428-aabdad7d4364
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CoGetObjectContext, CoGetObjectContext function [COM], _com_CoGetObjectContext, com.cogetobjectcontext, combaseapi/CoGetObjectContext
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
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetObjectContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
Before this function can be called, the <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> function must be called on the current thread.

</td>
</tr>
</table>
 




## -remarks



<b>CoGetObjectContext</b> retrieves the context for the object from which it is called, and returns a pointer to an interface that can be used to manipulate context properties. Context properties are used to provide services to configured components running within COM+ applications.

For components running within COM applications, the following interfaces are supported for accessing context properties: <a href="https://msdn.microsoft.com/fa4c7d82-ec5d-43d6-914e-bba60ad19aa2">IComThreadingInfo</a>, <a href="https://msdn.microsoft.com/89c41d9c-186c-4927-990d-92aa501f7d35">IContext</a>, and <a href="https://msdn.microsoft.com/47af7b80-3419-4a40-8932-a5a27f297dc9">IContextCallback</a>.

For components running within COM+ applications, the following interfaces are supported for accessing context properties: <a href="_cos_IObjectContext">IObjectContext</a>, <a href="_cos_IObjectContextActivity">IObjectContextActivity</a>, <a href="_cos_IObjectContextInfo">IObjectContextInfo</a>, and <a href="_cos_IContextState">IContextState</a>.




## -see-also




<a href="_cos_Contexts">Contexts and Threading Models</a>
 

 

