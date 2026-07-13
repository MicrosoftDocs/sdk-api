---
UID: NF:bdatif.ITuneRequestInfo.GetNextLocator
title: ITuneRequestInfo::GetNextLocator (bdatif.h)
description: The GetNextLocator method creates a new tune request with locator information for the next transport stream on the network.
helpviewer_keywords: ["GetNextLocator","GetNextLocator method [Microsoft TV Technologies]","GetNextLocator method [Microsoft TV Technologies]","ITuneRequestInfo interface","ITuneRequestInfo interface [Microsoft TV Technologies]","GetNextLocator method","ITuneRequestInfo.GetNextLocator","ITuneRequestInfo::GetNextLocator","ITuneRequestInfoGetNextLocator","bdatif/ITuneRequestInfo::GetNextLocator","mstv.itunerequestinfo_getnextlocator"]
old-location: mstv\itunerequestinfo_getnextlocator.htm
tech.root: mstv
ms.assetid: 300479bf-f8e3-41e2-898e-8a87e4abc801
ms.date: 12/05/2018
ms.keywords: GetNextLocator, GetNextLocator method [Microsoft TV Technologies], GetNextLocator method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],GetNextLocator method, ITuneRequestInfo.GetNextLocator, ITuneRequestInfo::GetNextLocator, ITuneRequestInfoGetNextLocator, bdatif/ITuneRequestInfo::GetNextLocator, mstv.itunerequestinfo_getnextlocator
req.header: bdatif.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITuneRequestInfo::GetNextLocator
 - bdatif/ITuneRequestInfo::GetNextLocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - ITuneRequestInfo.GetNextLocator
---

# ITuneRequestInfo::GetNextLocator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetNextLocator</b> method creates a new tune request with locator information for the next transport stream on the network.

## -parameters

### -param CurrentRequest [in]

Specifies the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface of the current tune request. <b>NULL</b> means to return information for the first stream.

### -param TuneRequest [out]

Pointer to a variable that receives a tune request for the next transport stream.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>CurrentRequest</i> is not valid, or <i>TuneRequest</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method is used internally by the Network Provider's <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtuner-seekup">IScanningTuner::SeekUp</a> and <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtuner-seekdown">IScanningTuner::SeekDown</a> methods, and is also useful for any Guide Store Loader that scans a network for EPG information.

Currently this method is not implemented for DVB-C or DVB-S networks, and the method returns E_NOTIMPL. The method is implemented for DVB-T.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-itunerequestinfo">ITuneRequestInfo Interface</a>