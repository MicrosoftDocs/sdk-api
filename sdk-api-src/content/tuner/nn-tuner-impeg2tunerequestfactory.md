---
UID: NN:tuner.IMPEG2TuneRequestFactory
title: IMPEG2TuneRequestFactory (tuner.h)
description: The IMPEG2TuneRequestFactory interface creates a tune request for a basic MPEG-2 transport stream containing the minimal tables. To obtain this interface, call CoCreateInstance with the class identifier CLSID_MPEG2TuneRequestFactory.helpviewer_keywords: ["IMPEG2TuneRequestFactory","IMPEG2TuneRequestFactory interface [Microsoft TV Technologies]","IMPEG2TuneRequestFactory interface [Microsoft TV Technologies]","described","IMPEG2TuneRequestFactoryInterface","mstv.impeg2tunerequestfactory","tuner/IMPEG2TuneRequestFactory"]
old-location: mstv\impeg2tunerequestfactory.htm
tech.root: mstv
ms.assetid: 0fbeab7d-0c54-45e3-a73c-755df28a16d5
ms.date: 12/05/2018
ms.keywords: IMPEG2TuneRequestFactory, IMPEG2TuneRequestFactory interface [Microsoft TV Technologies], IMPEG2TuneRequestFactory interface [Microsoft TV Technologies],described, IMPEG2TuneRequestFactoryInterface, mstv.impeg2tunerequestfactory, tuner/IMPEG2TuneRequestFactory
f1_keywords:
- tuner/IMPEG2TuneRequestFactory
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
- IMPEG2TuneRequestFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMPEG2TuneRequestFactory interface


## -description



The <b>IMPEG2TuneRequestFactory</b> interface creates a tune request for a basic MPEG-2 transport stream containing the minimal tables. To obtain this interface, call <b>CoCreateInstance</b> with the class identifier CLSID_MPEG2TuneRequestFactory.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2TuneRequestFactory</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMPEG2TuneRequestFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2TuneRequestFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2tunerequestfactory-createtunerequest">CreateTuneRequest</a>
</td>
<td align="left" width="63%">
Creates the minimal MPEG-2 tune request for a specified tuning space

</td>
</tr>
</table> 


## -remarks



To create a full tune request, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ibdacreatetunerequestex">CreateTuneRequest</a> method provided by one of the tuning space objects.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequestFactory)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

