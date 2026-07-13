---
UID: NF:bdatif.ITuneRequestInfo.GetNextProgram
title: ITuneRequestInfo::GetNextProgram (bdatif.h)
description: The GetNextProgram method creates a new tune request with channel or program locator information for the next service.
helpviewer_keywords: ["GetNextProgram","GetNextProgram method [Microsoft TV Technologies]","GetNextProgram method [Microsoft TV Technologies]","ITuneRequestInfo interface","ITuneRequestInfo interface [Microsoft TV Technologies]","GetNextProgram method","ITuneRequestInfo.GetNextProgram","ITuneRequestInfo::GetNextProgram","ITuneRequestInfoGetNextProgram","bdatif/ITuneRequestInfo::GetNextProgram","mstv.itunerequestinfo_getnextprogram"]
old-location: mstv\itunerequestinfo_getnextprogram.htm
tech.root: mstv
ms.assetid: ed1c5a30-19fb-46a8-b521-017da56d85c8
ms.date: 12/05/2018
ms.keywords: GetNextProgram, GetNextProgram method [Microsoft TV Technologies], GetNextProgram method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],GetNextProgram method, ITuneRequestInfo.GetNextProgram, ITuneRequestInfo::GetNextProgram, ITuneRequestInfoGetNextProgram, bdatif/ITuneRequestInfo::GetNextProgram, mstv.itunerequestinfo_getnextprogram
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
 - ITuneRequestInfo::GetNextProgram
 - bdatif/ITuneRequestInfo::GetNextProgram
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
 - ITuneRequestInfo.GetNextProgram
---

# ITuneRequestInfo::GetNextProgram


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetNextProgram</b> method creates a new tune request with channel or program locator information for the next service.

## -parameters

### -param CurrentRequest [in]

Specifies the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface of the current request.

### -param TuneRequest [out]

Pointer to a variable that will receive a tune request for the next service on the transport stream.

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

This method might be used by a custom Guide Store Loader to enumerate the available services on a transport stream.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-itunerequestinfo">ITuneRequestInfo Interface</a>