---
UID: NN:callobj.ICallIndirect
title: ICallIndirect
author: windows-sdk-content
description: Invokes an object with an indirect reference to the invocations arguments, rather than the traditional direct call.
old-location: com\icallindirect.htm
tech.root: com
ms.assetid: b85585fd-5f44-4c07-91a4-145eb44a6bdd
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ICallIndirect, ICallIndirect interface [COM], ICallIndirect interface [COM],described, _com_icallindirect_interface, callobj/ICallIndirect, com.icallindirect
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
 - ICallIndirect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallIndirect interface


## -description


Invokes an object with an indirect reference to the invocations arguments, rather than the traditional direct call. An instance of <b>ICallIndirect</b> supports indirect invocations for only one interface ID.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallIndirect</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICallIndirect</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICallIndirect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms693373(v=VS.85).aspx">CallIndirect</a>
</td>
<td align="left" width="63%">
Invokes one of the methods in the interface with an indirect reference to the arguments of the invocation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678487(v=VS.85).aspx">GetIID</a>
</td>
<td align="left" width="63%">
Retrieves the interface id supported by this <b>ICallIndirect</b> implementation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679729(v=VS.85).aspx">GetMethodInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the interface method from the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680134(v=VS.85).aspx">GetStackSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of bytes that should be popped from the stack in order to return from an invocation of the method.

</td>
</tr>
</table> 


## -remarks



The actual detailed semantics of how to carry out an indirect call are independent of the <b>ICallIndirect</b> interface itself; they are instead specific to the implementation of the interface. For example, implementations of <b>ICallIndirect</b> found in call interceptors carry out the call by constructing and appropriate <a href="https://msdn.microsoft.com/en-us/library/ms683709(v=VS.85).aspx">ICallFrame</a> instance and then invoking <a href="https://msdn.microsoft.com/en-us/library/ms692566(v=VS.85).aspx">ICallFrameEvents::OnCall</a> in the registered sink. Other implementations might do some appropriate munging of the invocations arguments, then forward the call on to some actual specific object, presumably one previously registered with the <b>ICallIndirect</b> using some implementation-specific means.






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms693378(v=VS.85).aspx">ICallInterceptor</a>
 

 

