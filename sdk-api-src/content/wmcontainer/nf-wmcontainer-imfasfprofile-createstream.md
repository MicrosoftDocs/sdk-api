---
UID: NF:wmcontainer.IMFASFProfile.CreateStream
title: IMFASFProfile::CreateStream (wmcontainer.h)
description: Creates an Advanced Systems Format (ASF) stream configuration object.
helpviewer_keywords: ["3da52c1a-24c0-456b-a9e8-57b5467eda2a","CreateStream","CreateStream method [Media Foundation]","CreateStream method [Media Foundation]","IMFASFProfile interface","IMFASFProfile interface [Media Foundation]","CreateStream method","IMFASFProfile.CreateStream","IMFASFProfile::CreateStream","mf.imfasfprofile_createstream","wmcontainer/IMFASFProfile::CreateStream"]
old-location: mf\imfasfprofile_createstream.htm
tech.root: mf
ms.assetid: 3da52c1a-24c0-456b-a9e8-57b5467eda2a
ms.date: 12/05/2018
ms.keywords: 3da52c1a-24c0-456b-a9e8-57b5467eda2a, CreateStream, CreateStream method [Media Foundation], CreateStream method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],CreateStream method, IMFASFProfile.CreateStream, IMFASFProfile::CreateStream, mf.imfasfprofile_createstream, wmcontainer/IMFASFProfile::CreateStream
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
 - IMFASFProfile::CreateStream
 - wmcontainer/IMFASFProfile::CreateStream
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
 - IMFASFProfile.CreateStream
---

# IMFASFProfile::CreateStream


## -description

Creates an Advanced Systems Format (ASF) stream configuration object.

## -parameters

### -param pIMediaType [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of a configured media type.

### -param ppIStream [out]

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a> interface of the new ASF stream configuration object. The caller must release the interface.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppIStream</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
stream configuration object could not be created due to insufficient memory.

</td>
</tr>
</table>

## -remarks

The ASF stream configuration object created by this method is not included in the profile. To include the stream, you must first configure the stream configuration and then call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream">IMFASFProfile::SetStream</a>.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>