---
UID: NN:tapi3if.ITMediaSupport
title: ITMediaSupport (tapi3if.h)
author: windows-sdk-content
description: The ITMediaSupport interface provides methods that allow an application to discover the media support capabilities for an Address Object that exposes this interface.
old-location: tapi3\itmediasupport.htm
tech.root: Tapi
ms.assetid: 196995f1-b8d0-4ec1-b94e-61a02a258087
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITMediaSupport, ITMediaSupport interface [TAPI 2.2], ITMediaSupport interface [TAPI 2.2],described, _tapi3_itmediasupport, tapi3.itmediasupport, tapi3if/ITMediaSupport
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITMediaSupport"
dev_langs:
 - c++
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMediaSupport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITMediaSupport interface


## -description


The 
<b>ITMediaSupport</b> interface provides methods that allow an application to discover the media support capabilities for an 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a> that exposes this interface. A pointer to this interface can be obtained by calling <b>QueryInterface</b> using any address interface pointer, such as 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMediaSupport</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITMediaSupport</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes">get_MediaTypes</a>
</td>
<td align="left" width="63%">
Gets 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">media types</a> supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-querymediatype">QueryMediaType</a>
</td>
<td align="left" width="63%">
Indicates whether a given media type is supported.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a>
 

 

