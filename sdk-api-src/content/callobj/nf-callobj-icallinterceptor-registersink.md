---
UID: NF:callobj.ICallInterceptor.RegisterSink
title: ICallInterceptor::RegisterSink
author: windows-sdk-content
description: Registers an event sink for receiving notifications of method calls.
old-location: com\icallinterceptor_registersink.htm
tech.root: com
ms.assetid: 07de2e42-0490-4801-8951-6e71ffb8ed93
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ICallInterceptor interface [COM],RegisterSink method, ICallInterceptor.RegisterSink, ICallInterceptor::RegisterSink, RegisterSink, RegisterSink method [COM], RegisterSink method [COM],ICallInterceptor interface, _com_icallinterceptor_registersink, callobj/ICallInterceptor::RegisterSink, com.icallinterceptor_registersink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallInterceptor.RegisterSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallInterceptor::RegisterSink


## -description


Registers an event sink for receiving notifications of method calls.

Only a single event sink may be registered with an interceptor at a time. Registering a sink of <b>NULL</b> is legal, and causes the interceptor to release any previously registered sink that it might be holding on to.


## -parameters




### -param psink [in]

A pointer to the event sink. See <a href="https://msdn.microsoft.com/2f1e1b8d-6150-45e9-89e2-524d80df558d">ICallFrameEvents</a>.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d0a72c87-598b-4ebe-bc93-65e0927a4c3d">ICallInterceptor</a>
 

 

