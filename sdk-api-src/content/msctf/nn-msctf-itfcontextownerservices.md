---
UID: NN:msctf.ITfContextOwnerServices
title: ITfContextOwnerServices (msctf.h)
description: The ITfContextOwnerServices interface is implemented by the manager and used by a text service or application acting as context owners.
old-location: tsf\itfcontextownerservices.htm
tech.root: TSF
ms.assetid: fb77bd6a-ae34-4e21-8f09-fc8c6a1ade86
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerServices, ITfContextOwnerServices interface [Text Services Framework], ITfContextOwnerServices interface [Text Services Framework],described, _tsf_itfcontextownerservices_ref, msctf/ITfContextOwnerServices, tsf.itfcontextownerservices
f1_keywords:
- msctf/ITfContextOwnerServices
dev_langs:
- c++
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITfContextOwnerServices
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfContextOwnerServices interface


## -description


The <b>ITfContextOwnerServices</b> interface is implemented by the manager and used by a text service or application acting as context owners. The interface provides notification changes to sinks and other services to context owners that do not implement the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> or <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a> interfaces. Clients obtain this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext::QueryInterface</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextOwnerServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextOwnerServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContextOwnerServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownerservices-createrange">CreateRange</a>
</td>
<td align="left" width="63%">
Creates a new range based upon a specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownerservices-forceloadproperty">ForceLoadProperty</a>
</td>
<td align="left" width="63%">
Forces a property load.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownerservices-onattributechange">OnAttributeChange</a>
</td>
<td align="left" width="63%">
Called by a context owner to generate notifications that a support attribute value changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownerservices-onlayoutchange">OnLayoutChange</a>
</td>
<td align="left" width="63%">
Called by the context owner when the on-screen representation of the text stream is updated during a composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownerservices-onstatuschange">OnStatusChange</a>
</td>
<td align="left" width="63%">
Called by the context owner when the dwDynamicFlags member of the TS_STATUS structure returned by the ITfContextOwner::GetStatus method changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownerservices-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Obtains a property from a range of text and writes the property data into a stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownerservices-unserialize">Unserialize</a>
</td>
<td align="left" width="63%">
Applies previously serialized property data to a property object.

</td>
</tr>
</table> 

