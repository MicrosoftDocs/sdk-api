---
UID: NF:wmcontainer.IMFASFStreamConfig.SetMediaType
title: IMFASFStreamConfig::SetMediaType (wmcontainer.h)
description: Sets the media type for the Advanced Systems Format (ASF) stream configuration object.
helpviewer_keywords: ["53b7c4fd-a3bc-4e15-b2f6-380cae8ab2f6","IMFASFStreamConfig interface [Media Foundation]","SetMediaType method","IMFASFStreamConfig.SetMediaType","IMFASFStreamConfig::SetMediaType","SetMediaType","SetMediaType method [Media Foundation]","SetMediaType method [Media Foundation]","IMFASFStreamConfig interface","mf.imfasfstreamconfig_setmediatype","wmcontainer/IMFASFStreamConfig::SetMediaType"]
old-location: mf\imfasfstreamconfig_setmediatype.htm
tech.root: mf
ms.assetid: 53b7c4fd-a3bc-4e15-b2f6-380cae8ab2f6
ms.date: 12/05/2018
ms.keywords: 53b7c4fd-a3bc-4e15-b2f6-380cae8ab2f6, IMFASFStreamConfig interface [Media Foundation],SetMediaType method, IMFASFStreamConfig.SetMediaType, IMFASFStreamConfig::SetMediaType, SetMediaType, SetMediaType method [Media Foundation], SetMediaType method [Media Foundation],IMFASFStreamConfig interface, mf.imfasfstreamconfig_setmediatype, wmcontainer/IMFASFStreamConfig::SetMediaType
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
 - IMFASFStreamConfig::SetMediaType
 - wmcontainer/IMFASFStreamConfig::SetMediaType
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
 - IMFASFStreamConfig.SetMediaType
---

# IMFASFStreamConfig::SetMediaType


## -description

Sets the media type for the Advanced Systems Format (ASF) stream configuration object.

## -parameters

### -param pIMediaType [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of a configured media type object.

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

Some validation of the media type is performed by this method. However, a media type can be successfully set, but cause an error when the stream is added to the profile.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype">IMFASFStreamConfig::GetMediaType</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>