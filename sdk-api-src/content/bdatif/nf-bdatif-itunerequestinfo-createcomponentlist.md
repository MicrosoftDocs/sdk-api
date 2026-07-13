---
UID: NF:bdatif.ITuneRequestInfo.CreateComponentList
title: ITuneRequestInfo::CreateComponentList (bdatif.h)
description: The CreateComponentList method creates a new Components collection for the tune request, and fills it in with all network-specific data after the receiver has tuned to the service.
helpviewer_keywords: ["CreateComponentList","CreateComponentList method [Microsoft TV Technologies]","CreateComponentList method [Microsoft TV Technologies]","ITuneRequestInfo interface","ITuneRequestInfo interface [Microsoft TV Technologies]","CreateComponentList method","ITuneRequestInfo.CreateComponentList","ITuneRequestInfo::CreateComponentList","ITuneRequestInfoCreateComponentList","bdatif/ITuneRequestInfo::CreateComponentList","mstv.itunerequestinfo_createcomponentlist"]
old-location: mstv\itunerequestinfo_createcomponentlist.htm
tech.root: mstv
ms.assetid: cb4ec234-1e94-4c9f-8372-a5972df18948
ms.date: 12/05/2018
ms.keywords: CreateComponentList, CreateComponentList method [Microsoft TV Technologies], CreateComponentList method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],CreateComponentList method, ITuneRequestInfo.CreateComponentList, ITuneRequestInfo::CreateComponentList, ITuneRequestInfoCreateComponentList, bdatif/ITuneRequestInfo::CreateComponentList, mstv.itunerequestinfo_createcomponentlist
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
 - ITuneRequestInfo::CreateComponentList
 - bdatif/ITuneRequestInfo::CreateComponentList
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
 - ITuneRequestInfo.CreateComponentList
---

# ITuneRequestInfo::CreateComponentList


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>CreateComponentList</b> method creates a new <a href="/previous-versions/windows/desktop/mstv/components-object">Components</a> collection for the tune request, and fills it in with all network-specific data after the receiver has tuned to the service.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No data could be acquired.

</td>
</tr>
</table>

## -remarks

After the Network Provider has acquired the correct transport stream, it asks the TIF to fill in the component data. If the tune request does not already have a components list, the Network Provider calls this method and asks the TIF to create one based on the relevant transport stream tables. Generally, the components will include one or more audio streams, video, data, and text. Each component has a component type, and on MPEG2 tuning spaces each component has an associated PID and pcrPID. Ideally, when the Guide Store Loader creates tune requests, it will include all the component information that is available.

The <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-itunerequestinfo-getcomponentdata">ITuneRequestInfo::GetComponentData</a> method is used to enable the TIF to change an existing list of components. S_FALSE indicates nothing was changed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-itunerequestinfo">ITuneRequestInfo Interface</a>