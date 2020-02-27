---
UID: NN:tapi3if.ITSubStreamControl
title: ITSubStreamControl (tapi3if.h)
description: The ITSubStreamControl interface exposes methods that allow an application to enumerate, create, or remove substreams. Many MSPs do not support this interface.
old-location: tapi3\itsubstreamcontrol.htm
tech.root: Tapi
ms.assetid: 17c5f2ba-d526-4b00-9649-8fd73d70bc79
ms.date: 12/05/2018
ms.keywords: ITSubStreamControl, ITSubStreamControl interface [TAPI 2.2], ITSubStreamControl interface [TAPI 2.2],described, _tapi3_itsubstreamcontrol, tapi3.itsubstreamcontrol, tapi3if/ITSubStreamControl
f1_keywords:
- tapi3if/ITSubStreamControl
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
- ITSubStreamControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSubStreamControl interface


## -description


The 
<b>ITSubStreamControl</b> interface exposes methods that allow an application to enumerate, create, or remove substreams. Many MSPs do not support this interface.

A pointer to this interface can be obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the stream object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSubStreamControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITSubStreamControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSubStreamControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itsubstreamcontrol-createsubstream">CreateSubStream</a>
</td>
<td align="left" width="63%">
Creates a substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itsubstreamcontrol-enumeratesubstreams">EnumerateSubStreams</a>
</td>
<td align="left" width="63%">
Enumerates substreams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itsubstreamcontrol-get_substreams">get_SubStreams</a>
</td>
<td align="left" width="63%">
Creates a collection of substreams associated with the current stream. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itsubstreamcontrol-removesubstream">RemoveSubStream</a>
</td>
<td align="left" width="63%">
Removes a substream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
 

 

