---
UID: NN:tapi3if.ITStreamControl
title: ITStreamControl (tapi3if.h)
description: The ITStreamControl interface represents the media streaming features of a call and exposes methods that allow an application to enumerate, create, or remove streams.helpviewer_keywords: ["ITStreamControl","ITStreamControl interface [TAPI 2.2]","ITStreamControl interface [TAPI 2.2]","described","_tapi3_itstreamcontrol","tapi3.itstreamcontrol","tapi3if/ITStreamControl"]
old-location: tapi3\itstreamcontrol.htm
tech.root: Tapi
ms.assetid: 12b9457a-7afb-4348-93a2-28728c673929
ms.date: 12/05/2018
ms.keywords: ITStreamControl, ITStreamControl interface [TAPI 2.2], ITStreamControl interface [TAPI 2.2],described, _tapi3_itstreamcontrol, tapi3.itstreamcontrol, tapi3if/ITStreamControl
f1_keywords:
- tapi3if/ITStreamControl
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
- ITStreamControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITStreamControl interface


## -description


The 
<b>ITStreamControl</b> interface represents the media streaming features of a call and exposes methods that allow an application to enumerate, create, or remove streams.

If this interface exists, a TAPI application acquires a pointer to this interface by performing a <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on any call interface, such as 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>. This interface is not available if an MSP is not involved in the current call session.

Internal to the TAPI DLL, this interface is implemented by the MSP's call object, which is created in the 
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall">ITMSPAddress::CreateMSPCall</a> method. TAPI then aggregates this interface onto the TAPI call object and exposes it to TAPI applications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITStreamControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITStreamControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITStreamControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream">CreateStream</a>
</td>
<td align="left" width="63%">
Creates a media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-enumeratestreams">EnumerateStreams</a>
</td>
<td align="left" width="63%">
Enumerates streams currently available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-get_streams">get_Streams</a>
</td>
<td align="left" width="63%">
Creates a collection of streams currently available. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-removestream">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a media stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
 

 

