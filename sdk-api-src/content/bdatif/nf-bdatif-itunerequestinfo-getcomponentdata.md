---
UID: NF:bdatif.ITuneRequestInfo.GetComponentData
title: ITuneRequestInfo::GetComponentData (bdatif.h)
description: The GetComponentData method fills in all network-specific component data for the existing Components collection on the specified tune request.
helpviewer_keywords: ["GetComponentData","GetComponentData method [Microsoft TV Technologies]","GetComponentData method [Microsoft TV Technologies]","ITuneRequestInfo interface","ITuneRequestInfo interface [Microsoft TV Technologies]","GetComponentData method","ITuneRequestInfo.GetComponentData","ITuneRequestInfo::GetComponentData","ITuneRequestInfoGetComponentData","bdatif/ITuneRequestInfo::GetComponentData","mstv.itunerequestinfo_getcomponentdata"]
old-location: mstv\itunerequestinfo_getcomponentdata.htm
tech.root: mstv
ms.assetid: 769d112e-4df7-451c-ac12-440b16c33e88
ms.date: 12/05/2018
ms.keywords: GetComponentData, GetComponentData method [Microsoft TV Technologies], GetComponentData method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],GetComponentData method, ITuneRequestInfo.GetComponentData, ITuneRequestInfo::GetComponentData, ITuneRequestInfoGetComponentData, bdatif/ITuneRequestInfo::GetComponentData, mstv.itunerequestinfo_getcomponentdata
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
 - ITuneRequestInfo::GetComponentData
 - bdatif/ITuneRequestInfo::GetComponentData
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
 - ITuneRequestInfo.GetComponentData
---

# ITuneRequestInfo::GetComponentData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetComponentData</b> method fills in all network-specific component data for the existing <a href="/previous-versions/windows/desktop/mstv/components-object">Components</a> collection on the specified tune request.

## -parameters

### -param CurrentRequest [in]

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
The method succeeded and new data was added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded but no new data was added.

</td>
</tr>
</table>

## -remarks

The Network Provider calls this method after the tuner has tuned to the specified service.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-itunerequestinfo">ITuneRequestInfo Interface</a>