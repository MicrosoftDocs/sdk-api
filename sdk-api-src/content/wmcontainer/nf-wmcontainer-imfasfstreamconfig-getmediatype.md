---
UID: NF:wmcontainer.IMFASFStreamConfig.GetMediaType
title: IMFASFStreamConfig::GetMediaType (wmcontainer.h)
description: Retrieves the media type of the stream.
helpviewer_keywords: ["6311115a-26e6-47b7-b724-0209a5bf45d7","GetMediaType","GetMediaType method [Media Foundation]","GetMediaType method [Media Foundation]","IMFASFStreamConfig interface","IMFASFStreamConfig interface [Media Foundation]","GetMediaType method","IMFASFStreamConfig.GetMediaType","IMFASFStreamConfig::GetMediaType","mf.imfasfstreamconfig_getmediatype","wmcontainer/IMFASFStreamConfig::GetMediaType"]
old-location: mf\imfasfstreamconfig_getmediatype.htm
tech.root: mf
ms.assetid: 6311115a-26e6-47b7-b724-0209a5bf45d7
ms.date: 12/05/2018
ms.keywords: 6311115a-26e6-47b7-b724-0209a5bf45d7, GetMediaType, GetMediaType method [Media Foundation], GetMediaType method [Media Foundation],IMFASFStreamConfig interface, IMFASFStreamConfig interface [Media Foundation],GetMediaType method, IMFASFStreamConfig.GetMediaType, IMFASFStreamConfig::GetMediaType, mf.imfasfstreamconfig_getmediatype, wmcontainer/IMFASFStreamConfig::GetMediaType
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFStreamConfig::GetMediaType
 - wmcontainer/IMFASFStreamConfig::GetMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamConfig.GetMediaType
---

# IMFASFStreamConfig::GetMediaType


## -description

Retrieves the media type of the stream.

## -parameters

### -param ppIMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type object associated with the stream. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -remarks

To reduce unnecessary copying, the method returns a pointer to the media type  that is stored internally by the object. Do not modify the returned media type,  as the results are not defined.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype">IMFASFStreamConfig::SetMediaType</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>