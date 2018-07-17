---
UID: NN:callobj.ICallInterceptor
title: ICallInterceptor
author: windows-sdk-content
description: Supports the registration and un-registering of event sinks wishing to be notified of calls made directly on the interface.
old-location: com\icallinterceptor.htm
old-project: com
ms.assetid: d0a72c87-598b-4ebe-bc93-65e0927a4c3d
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICallInterceptor, ICallInterceptor interface [COM], ICallInterceptor interface [COM],described, _com_icallinterceptor_interface, callobj/ICallInterceptor, com.icallinterceptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: CALLFRAME_COPY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallInterceptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICallInterceptor interface


## -description


Supports the registration and un-registering of event sinks wishing to be notified of calls made directly on the interface. In addition, this interface provides a means by which an invocation can be carried out with an indirect reference to the invocations arguments.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallInterceptor</b> interface inherits from <b>ICallIndirect</b>. <b>ICallInterceptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICallInterceptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65f33bc3-9fcb-4ad5-908d-3ac06b9f8c6c">GetRegisteredSink</a>
</td>
<td align="left" width="63%">
Retrieves the registered event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07de2e42-0490-4801-8951-6e71ffb8ed93">RegisterSink</a>
</td>
<td align="left" width="63%">
Registers an event sink for receiving notifications of method calls.

</td>
</tr>
</table> 

