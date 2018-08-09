---
UID: NN:tapi3if.ITMediaSupport
title: ITMediaSupport
author: windows-sdk-content
description: The ITMediaSupport interface provides methods that allow an application to discover the media support capabilities for an Address Object that exposes this interface.
old-location: tapi3\itmediasupport.htm
old-project: tapi
ms.assetid: 196995f1-b8d0-4ec1-b94e-61a02a258087
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITMediaSupport, ITMediaSupport interface [TAPI 2.2], ITMediaSupport interface [TAPI 2.2],described, _tapi3_itmediasupport, tapi3.itmediasupport, tapi3if/ITMediaSupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMediaSupport
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITMediaSupport interface


## -description


The 
<b>ITMediaSupport</b> interface provides methods that allow an application to discover the media support capabilities for an 
<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a> that exposes this interface. A pointer to this interface can be obtained by calling <b>QueryInterface</b> using any address interface pointer, such as 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMediaSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITMediaSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITMediaSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fc3d82e-6d6f-4442-9232-87f8d7605870">get_MediaTypes</a>
</td>
<td align="left" width="63%">
Gets 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/684bfd94-5bef-415b-b548-49f564ce8a83">QueryMediaType</a>
</td>
<td align="left" width="63%">
Indicates whether a given media type is supported.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>



<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a>
 

 

