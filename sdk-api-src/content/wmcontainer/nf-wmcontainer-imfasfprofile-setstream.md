---
UID: NF:wmcontainer.IMFASFProfile.SetStream
title: IMFASFProfile::SetStream (wmcontainer.h)
description: Adds a stream to the profile or reconfigures an existing stream.
helpviewer_keywords: ["IMFASFProfile interface [Media Foundation]","SetStream method","IMFASFProfile.SetStream","IMFASFProfile::SetStream","SetStream","SetStream method [Media Foundation]","SetStream method [Media Foundation]","IMFASFProfile interface","c2272260-74ab-42ff-bff3-d6c6d5b322f3","mf.imfasfprofile_setstream","wmcontainer/IMFASFProfile::SetStream"]
old-location: mf\imfasfprofile_setstream.htm
tech.root: mf
ms.assetid: c2272260-74ab-42ff-bff3-d6c6d5b322f3
ms.date: 12/05/2018
ms.keywords: IMFASFProfile interface [Media Foundation],SetStream method, IMFASFProfile.SetStream, IMFASFProfile::SetStream, SetStream, SetStream method [Media Foundation], SetStream method [Media Foundation],IMFASFProfile interface, c2272260-74ab-42ff-bff3-d6c6d5b322f3, mf.imfasfprofile_setstream, wmcontainer/IMFASFProfile::SetStream
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
 - IMFASFProfile::SetStream
 - wmcontainer/IMFASFProfile::SetStream
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
 - IMFASFProfile.SetStream
---

# IMFASFProfile::SetStream


## -description

Adds a stream to the profile or reconfigures an existing stream.

## -parameters

### -param pIStream [in]

Pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a> interface of a configured ASF stream configuration object.

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

If the stream number in the ASF stream configuration object is already included in the profile, the information in the new object replaces the old one. If the profile does not contain a stream for the stream number, the ASF stream configuration object is added as a new stream.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream">IMFASFProfile::GetStream</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber">IMFASFProfile::GetStreamByNumber</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount">IMFASFProfile::GetStreamCount</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream">IMFASFProfile::RemoveStream</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>