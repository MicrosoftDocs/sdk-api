---
UID: NN:objidlbase.ICancelMethodCalls
title: ICancelMethodCalls
author: windows-driver-content
description: Manages cancellation requests on an outbound method call and monitors the current state of that method call on the server thread.
old-location: com\icancelmethodcalls.htm
old-project: com
ms.assetid: 5e31f706-1c9c-4510-845c-4e47093780a1
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ICancelMethodCalls, ICancelMethodCalls interface [COM], ICancelMethodCalls interface [COM],described, _com_icancelmethodcalls, com.icancelmethodcalls, objidlbase/ICancelMethodCalls
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	ICancelMethodCalls
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ICancelMethodCalls interface


## -description


Manages cancellation requests on an outbound method call and monitors the current state of that method call on the server thread.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICancelMethodCalls</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ICancelMethodCalls</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICancelMethodCalls</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Requests that a method call be canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31141d97-241e-4717-b707-e37d86c2267d">TestCancel</a>
</td>
<td align="left" width="63%">
Determines whether a call has been canceled.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a>
 

 

