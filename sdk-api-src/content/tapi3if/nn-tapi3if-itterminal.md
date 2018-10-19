---
UID: NN:tapi3if.ITTerminal
title: ITTerminal
author: windows-sdk-content
description: The ITTerminal interface is the base interface for a Terminal object.
old-location: tapi3\itterminal.htm
tech.root: TAPI
ms.assetid: 38bc30fa-3e4e-417a-9d04-931ba2451fa4
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITTerminal, ITTerminal interface [TAPI 2.2], ITTerminal interface [TAPI 2.2],described, _tapi3_itterminal, tapi3.itterminal, tapi3if/ITTerminal
ms.prod: windows
ms.technology: windows-sdk
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
 - ITTerminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminal interface


## -description


The 
<b>ITTerminal</b> interface is the base interface for a 
<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal object</a>. This object, and the interface, is available only when an MSP exists. It provides methods that allow an application to obtain information such as terminal class and media supported. The following methods create the 
<b>ITTerminal</b> interface:


<a href="https://msdn.microsoft.com/20b7266c-8990-457c-94cf-18cc2bed6b21">ITBasicCallControl2::RequestTerminal</a>



<a href="https://msdn.microsoft.com/2a2a037a-753c-4dd4-b6ce-10b69f2e2421">ITTerminalSupport::CreateTerminal</a>



<a href="https://msdn.microsoft.com/d419fd5e-2e08-4d41-93c2-062cd86973f4">IEnumTerminal::Next</a>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminal</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITTerminal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTerminal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0a69c3d-1780-4088-8249-961788dbf184">get_Direction</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor of the media stream direction for the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c2006ad-d2f9-4e21-b0ae-583ec3ff82f4">get_MediaType</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad3a44ff-ad63-4fd0-9cfd-c97c0cea6162">get_Name</a>
</td>
<td align="left" width="63%">
Gets a descriptive name of the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18eebe2c-2c65-4836-a371-146eb76a379c">get_State</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/310c41f5-dfe7-491d-8669-87a98694f5b7">TERMINAL_STATE</a> descriptor of the terminal's current state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a31543da-4cb8-4719-8e33-fcb4d9d630b1">get_TerminalClass</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">terminal class</a> of the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6f33151-2415-4f24-b84b-7f2ce724db5b">get_TerminalType</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/43d08be3-c09b-4c74-ad71-6b452850d2e0">TERMINAL_TYPE</a> descriptor of the terminal's type.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

