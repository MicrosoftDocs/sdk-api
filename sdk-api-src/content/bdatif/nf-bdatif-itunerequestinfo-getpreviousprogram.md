---
UID: NF:bdatif.ITuneRequestInfo.GetPreviousProgram
title: ITuneRequestInfo::GetPreviousProgram (bdatif.h)
description: The GetPreviousProgram method creates a new tune request with channel or program locator information for the previous service.
helpviewer_keywords: ["GetPreviousProgram","GetPreviousProgram method [Microsoft TV Technologies]","GetPreviousProgram method [Microsoft TV Technologies]","ITuneRequestInfo interface","ITuneRequestInfo interface [Microsoft TV Technologies]","GetPreviousProgram method","ITuneRequestInfo.GetPreviousProgram","ITuneRequestInfo::GetPreviousProgram","ITuneRequestInfoGetPreviousProgram","bdatif/ITuneRequestInfo::GetPreviousProgram","mstv.itunerequestinfo_getpreviousprogram"]
old-location: mstv\itunerequestinfo_getpreviousprogram.htm
tech.root: mstv
ms.assetid: 9c03a5c9-9dc1-4163-bbc8-8dae2037eb24
ms.date: 12/05/2018
ms.keywords: GetPreviousProgram, GetPreviousProgram method [Microsoft TV Technologies], GetPreviousProgram method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],GetPreviousProgram method, ITuneRequestInfo.GetPreviousProgram, ITuneRequestInfo::GetPreviousProgram, ITuneRequestInfoGetPreviousProgram, bdatif/ITuneRequestInfo::GetPreviousProgram, mstv.itunerequestinfo_getpreviousprogram
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
 - ITuneRequestInfo::GetPreviousProgram
 - bdatif/ITuneRequestInfo::GetPreviousProgram
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
 - ITuneRequestInfo.GetPreviousProgram
---

# ITuneRequestInfo::GetPreviousProgram


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetPreviousProgram</b> method creates a new tune request with channel or program locator information for the previous service.

## -parameters

### -param CurrentRequest [in]

Specifies the current request.

### -param TuneRequest [out]

Pointer to a variable that receives a tune request for the previous service in the current transport stream.

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