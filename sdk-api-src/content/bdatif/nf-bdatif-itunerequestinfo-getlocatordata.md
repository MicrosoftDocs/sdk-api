---
UID: NF:bdatif.ITuneRequestInfo.GetLocatorData
title: ITuneRequestInfo::GetLocatorData (bdatif.h)
description: The GetLocatorData method fills in channel or program locator information for the specified tune request.
helpviewer_keywords: ["GetLocatorData","GetLocatorData method [Microsoft TV Technologies]","GetLocatorData method [Microsoft TV Technologies]","ITuneRequestInfo interface","ITuneRequestInfo interface [Microsoft TV Technologies]","GetLocatorData method","ITuneRequestInfo.GetLocatorData","ITuneRequestInfo::GetLocatorData","ITuneRequestInfoGetLocatorData","bdatif/ITuneRequestInfo::GetLocatorData","mstv.itunerequestinfo_getlocatordata"]
old-location: mstv\itunerequestinfo_getlocatordata.htm
tech.root: mstv
ms.assetid: c325d61d-c99b-4033-bd16-36b74fc38d07
ms.date: 12/05/2018
ms.keywords: GetLocatorData, GetLocatorData method [Microsoft TV Technologies], GetLocatorData method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],GetLocatorData method, ITuneRequestInfo.GetLocatorData, ITuneRequestInfo::GetLocatorData, ITuneRequestInfoGetLocatorData, bdatif/ITuneRequestInfo::GetLocatorData, mstv.itunerequestinfo_getlocatordata
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
 - ITuneRequestInfo::GetLocatorData
 - bdatif/ITuneRequestInfo::GetLocatorData
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
 - ITuneRequestInfo.GetLocatorData
---

# ITuneRequestInfo::GetLocatorData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetLocatorData</b> method fills in channel or program locator information for the specified tune request.

## -parameters

### -param Request [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface on the tune request.

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
The method succeeded and new locator data was acquired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded but no new locator data was acquired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>Request</i> is not valid.

</td>
</tr>
</table>

## -remarks

After the TIF fills in the locator information, the Network Provider uses that information to configure the tuner and demodulator. It is expected that the TIF will always know everything about a locator. If it doesn't know how to locate a specific tune request, it can always fall back to the default locator for the tuning space. As soon as the TIF starts getting tables from the default stream, it signals the Network Provider, which then asks for the new locator data. When the TIF fills that in, it signals the Network Provider, which tunes again using the new information. When the TIF begins getting tables on the new stream, it signals the Network Provider again, and the process is repeated.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-itunerequestinfo">ITuneRequestInfo Interface</a>