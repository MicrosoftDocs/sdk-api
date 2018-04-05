---
UID: NF:urlmon.CreateAsyncBindCtx
title: CreateAsyncBindCtx function
author: windows-driver-content
description: Creates an asynchronous bind context for use with asynchronous monikers.
old-location: com\createasyncbindctx.htm
old-project: com
ms.assetid: 0c79b61b-d3d6-48fd-aaee-21cddad09208
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: CreateAsyncBindCtx, CreateAsyncBindCtx function [COM], _com_CreateAsyncBindCtx, com.createasyncbindctx, urlmon/CreateAsyncBindCtx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: urlmon.h
req.include-header: 
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
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Urlmon.dll
api_name:
-	CreateAsyncBindCtx
product: Windows
targetos: Windows
req.lib: Urlmon.lib
req.dll: Urlmon.dll
req.irql: 
req.product: Windows UI
---

# CreateAsyncBindCtx function


## -description


Creates an asynchronous bind context for use with asynchronous monikers.


## -parameters




### -param reserved [in]

This parameter is reserved and must be 0.


### -param pBSCb [in]

A pointer to the <a href="_inet_IBindStatusCallback_Interface_cpp">IBindStatusCallback</a> interface used for receiving data availability and progress notification.


### -param pEFetc [in]

A pointer to the <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> interface that can be used to enumerate formats for format negotiation during binding. This parameter can be <b>NULL</b>, in which case the caller is not interested in format negotiation during binding, and the default format of the object will be bound to.


### -param ppBC [out]

Address of an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>* pointer variable that receives the interface pointer to the new bind context.


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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY </b></dt>
</dl>
</td>
<td width="60%">
The method ran out of memory and did not complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



This function automatically registers the <a href="_inet_IBindStatusCallback_Interface_cpp">IBindStatusCallback</a> and <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> interfaces with the bind context. The client can specify flags from <a href="https://msdn.microsoft.com/82ca0285-5a03-40ab-b244-72e853e2a14a">BSCO_OPTION</a> to indicate which callback notifications the client is capable of receiving. If the client does not wish to receive certain notification, it can choose to implement those callback methods as empty function stubs (returning E_NOTIMPL), and they should not be called.

The <a href="_inet_RegisterBindStatusCallback_Function_cpp">RegisterBindStatusCallback</a> function can also be used to register callback interfaces in the bind context.





## -see-also




<a href="_inet_IBindStatusCallback_Interface_cpp">IBindStatusCallback</a>



<a href="_inet_RegisterBindStatusCallback_Function_cpp">RegisterBindStatusCallback</a>
 

 

