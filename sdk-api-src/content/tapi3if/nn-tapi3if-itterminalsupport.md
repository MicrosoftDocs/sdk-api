---
UID: NN:tapi3if.ITTerminalSupport
title: ITTerminalSupport (tapi3if.h)
author: windows-sdk-content
description: The ITTerminalSupport interface is exposed on an Address object only if an MSP exists. The methods of this interface allow an application to discover available terminals and/or create one, and get pointers to required Terminal objects.
old-location: tapi3\itterminalsupport.htm
tech.root: Tapi
ms.assetid: 8669324a-5c2c-4ed8-be24-a0c71fbb8c01
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITTerminalSupport, ITTerminalSupport interface [TAPI 2.2], ITTerminalSupport interface [TAPI 2.2],described, _tapi3_itterminalsupport, tapi3.itterminalsupport, tapi3if/ITTerminalSupport
ms.topic: interface
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Tapi3if.h
api_name:
 - ITTerminalSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalSupport interface


## -description


The 
<b>ITTerminalSupport</b> interface is exposed on an 
<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a> only if an MSP exists. The methods of this interface allow an application to discover available terminals and/or create one, and get pointers to required 
<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal objects</a>.

An 
tapi3.itterminalsupport pointer can be obtained by calling 
<a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> on any Address interface, such as 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>. If E_NOINTERFACE is returned, the service provider associated with the address does not support media controls.

The 
<a href="https://msdn.microsoft.com/58611991-746c-4626-a1b1-535a2134ee27">ITTerminalSupport2</a> interface is derived from the 
<b>ITTerminalSupport</b> interface. 
<b>ITTerminalSupport2</b> supports the retrieval of information about pluggable terminal classes and superclasses by C, C++, and scripting applications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminalSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITTerminalSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTerminalSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a2a037a-753c-4dd4-b6ce-10b69f2e2421">CreateTerminal</a>
</td>
<td align="left" width="63%">
Creates a new terminal based on the dynamic terminal class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1dcb9163-306b-42fc-afb4-41b33d7e2d40">EnumerateDynamicTerminalClasses</a>
</td>
<td align="left" width="63%">
Enumerates the currently available dynamic terminal classes that are supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91fea706-9792-40e1-b812-f7578bc7968b">EnumerateStaticTerminals</a>
</td>
<td align="left" width="63%">
Enumerates the currently available static terminals that are associated with the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/258fad5c-6269-45ab-bdc0-d38338f8e515">get_DynamicTerminalClasses</a>
</td>
<td align="left" width="63%">
Creates a collection of currently available dynamic terminals. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4cdd3f5-ca8c-4660-b37c-c38779a516dd">get_StaticTerminals</a>
</td>
<td align="left" width="63%">
Creates a collection of the currently available static terminals. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aad3a566-eb95-402c-b26f-da6bd89e52ea">GetDefaultStaticTerminal</a>
</td>
<td align="left" width="63%">
Gets the default static terminal for the media specified.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/58611991-746c-4626-a1b1-535a2134ee27">ITTerminalSupport2</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

