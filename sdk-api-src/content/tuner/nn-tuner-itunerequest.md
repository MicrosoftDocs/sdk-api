---
UID: NN:tuner.ITuneRequest
title: ITuneRequest (tuner.h)
description: The ITuneRequest interface is the base interface for all tune requests.
helpviewer_keywords: ["ITuneRequest","ITuneRequest interface [Microsoft TV Technologies]","ITuneRequest interface [Microsoft TV Technologies]","described","ITuneRequestInterface","mstv.itunerequest","tuner/ITuneRequest"]
old-location: mstv\itunerequest.htm
tech.root: mstv
ms.assetid: 34077b45-32b4-466b-b103-6a42fc869265
ms.date: 12/05/2018
ms.keywords: ITuneRequest, ITuneRequest interface [Microsoft TV Technologies], ITuneRequest interface [Microsoft TV Technologies],described, ITuneRequestInterface, mstv.itunerequest, tuner/ITuneRequest
f1_keywords:
- tuner/ITuneRequest
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
- tuner.h
api_name:
- ITuneRequest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuneRequest interface


## -description



The <b>ITuneRequest</b> interface is the base interface for all tune requests. Each tune request object supports a network-specific interface that derives from <b>ITuneRequest</b>, such as <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtunerequest">IDVBTuneRequest</a>.

This interface is used by any application that creates tune requests, such as a Guide Store loader. A tune request must be associated with a specific network type. When a tune request is submitted, the derived interfaces are used by the Network Provider to extract the tuning information required by the hardware. All tune request objects also support <b>IPersistPropertyBag</b>, which enables them to be persisted in some type of third-party storage mechanism.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuneRequest</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITuneRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITuneRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-itunerequest-clone">Clone</a>
</td>
<td align="left" width="63%">
Returns a new copy of this tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-itunerequest-get_components">get_Components</a>
</td>
<td align="left" width="63%">
Retrieves the components contained in this tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-itunerequest-get_locator">get_Locator</a>
</td>
<td align="left" width="63%">
Called from the Network Provider to get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a> object associated with the requested broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-itunerequest-get_tuningspace">get_TuningSpace</a>
</td>
<td align="left" width="63%">
Retrieves the tuning space that was used to create this tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-itunerequest-put_locator">put_Locator</a>
</td>
<td align="left" width="63%">
Called from the Network Provider to set the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a> object associated with the requested broadcast.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuneRequest)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

