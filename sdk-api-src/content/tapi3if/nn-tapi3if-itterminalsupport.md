---
UID: NN:tapi3if.ITTerminalSupport
title: ITTerminalSupport (tapi3if.h)
description: The ITTerminalSupport interface is exposed on an Address object only if an MSP exists. The methods of this interface allow an application to discover available terminals and/or create one, and get pointers to required Terminal objects.helpviewer_keywords: ["ITTerminalSupport","ITTerminalSupport interface [TAPI 2.2]","ITTerminalSupport interface [TAPI 2.2]","described","_tapi3_itterminalsupport","tapi3.itterminalsupport","tapi3if/ITTerminalSupport"]
old-location: tapi3\itterminalsupport.htm
tech.root: Tapi
ms.assetid: 8669324a-5c2c-4ed8-be24-a0c71fbb8c01
ms.date: 12/05/2018
ms.keywords: ITTerminalSupport, ITTerminalSupport interface [TAPI 2.2], ITTerminalSupport interface [TAPI 2.2],described, _tapi3_itterminalsupport, tapi3.itterminalsupport, tapi3if/ITTerminalSupport
f1_keywords:
- tapi3if/ITTerminalSupport
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITTerminalSupport interface


## -description


The 
<b>ITTerminalSupport</b> interface is exposed on an 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address object</a> only if an MSP exists. The methods of this interface allow an application to discover available terminals and/or create one, and get pointers to required 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal objects</a>.

An 
tapi3.itterminalsupport pointer can be obtained by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on any Address interface, such as 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>. If E_NOINTERFACE is returned, the service provider associated with the address does not support media controls.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2">ITTerminalSupport2</a> interface is derived from the 
<b>ITTerminalSupport</b> interface. 
<b>ITTerminalSupport2</b> supports the retrieval of information about pluggable terminal classes and superclasses by C, C++, and scripting applications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminalSupport</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTerminalSupport</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal">CreateTerminal</a>
</td>
<td align="left" width="63%">
Creates a new terminal based on the dynamic terminal class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses">EnumerateDynamicTerminalClasses</a>
</td>
<td align="left" width="63%">
Enumerates the currently available dynamic terminal classes that are supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals">EnumerateStaticTerminals</a>
</td>
<td align="left" width="63%">
Enumerates the currently available static terminals that are associated with the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses">get_DynamicTerminalClasses</a>
</td>
<td align="left" width="63%">
Creates a collection of currently available dynamic terminals. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals">get_StaticTerminals</a>
</td>
<td align="left" width="63%">
Creates a collection of the currently available static terminals. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-getdefaultstaticterminal">GetDefaultStaticTerminal</a>
</td>
<td align="left" width="63%">
Gets the default static terminal for the media specified.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2">ITTerminalSupport2</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>
 

 

