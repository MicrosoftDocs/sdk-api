---
UID: NN:tuner.IMPEG2TuneRequest
title: IMPEG2TuneRequest (tuner.h)

description: The IMPEG2TuneRequest interface represents a tune request for a basic MPEG-2 transport stream containing the minimal tables.Use the IMPEG2TuneRequestFactory::CreateTuneRequest method to obtain this interface.
old-location: mstv\impeg2tunerequest.htm
tech.root: mstv
ms.assetid: a9e37b8b-9272-43c6-b36e-1e82b0d1b0db

ms.date: 12/05/2018
ms.keywords: IMPEG2TuneRequest, IMPEG2TuneRequest interface [Microsoft TV Technologies], IMPEG2TuneRequest interface [Microsoft TV Technologies],described, IMPEG2TuneRequestInterface, mstv.impeg2tunerequest, tuner/IMPEG2TuneRequest
ms.topic: interface
f1_keywords: 
 - "tuner/IMPEG2TuneRequest"
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
 - IMPEG2TuneRequest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMPEG2TuneRequest interface


## -description



The <b>IMPEG2TuneRequest</b> interface represents a tune request for a basic MPEG-2 transport stream containing the minimal tables.

Use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2tunerequestfactory-createtunerequest">IMPEG2TuneRequestFactory::CreateTuneRequest</a> method to obtain this interface. It returns the minimal MPEG-2 tune request for a specified tuning space. To create a full tune request, use the <b>CreateTuneRequest</b> method provided by one of the tuning space objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2TuneRequest</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a>. <b>IMPEG2TuneRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2TuneRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2tunerequest-get_progno">get_ProgNo</a>
</td>
<td align="left" width="63%">
Retrieves the program number ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2tunerequest-get_tsid">get_TSID</a>
</td>
<td align="left" width="63%">
Retrieves the transport stream ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2tunerequest-put_progno">put_ProgNo</a>
</td>
<td align="left" width="63%">
Sets the program number ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2tunerequest-put_tsid">put_TSID</a>
</td>
<td align="left" width="63%">
Sets the transport stream ID.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequest)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

