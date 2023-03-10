---
UID: NF:wmcontainer.IMFASFProfile.GetStream
title: IMFASFProfile::GetStream (wmcontainer.h)
description: Retrieves a stream from the profile by stream index, and/or retrieves the stream number for a stream index.
helpviewer_keywords: ["918f6534-811e-42f6-9836-1c77816007fa","GetStream","GetStream method [Media Foundation]","GetStream method [Media Foundation]","IMFASFProfile interface","IMFASFProfile interface [Media Foundation]","GetStream method","IMFASFProfile.GetStream","IMFASFProfile::GetStream","mf.imfasfprofile_getstream","wmcontainer/IMFASFProfile::GetStream"]
old-location: mf\imfasfprofile_getstream.htm
tech.root: mf
ms.assetid: 918f6534-811e-42f6-9836-1c77816007fa
ms.date: 12/05/2018
ms.keywords: 918f6534-811e-42f6-9836-1c77816007fa, GetStream, GetStream method [Media Foundation], GetStream method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],GetStream method, IMFASFProfile.GetStream, IMFASFProfile::GetStream, mf.imfasfprofile_getstream, wmcontainer/IMFASFProfile::GetStream
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
 - IMFASFProfile::GetStream
 - wmcontainer/IMFASFProfile::GetStream
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
 - IMFASFProfile.GetStream
---

# IMFASFProfile::GetStream


## -description

Retrieves a stream from the profile by stream index, and/or retrieves the stream number for a stream index.

## -parameters

### -param dwStreamIndex [in]

The index of the stream to retrieve. Stream indexes are sequential and zero-based. You can get the number of streams that are in the profile by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount">IMFASFProfile::GetStreamCount</a> method.

### -param pwStreamNumber [out]

Receives the stream number of the requested stream. Stream numbers are one-based and are not necessarily sequential. This parameter can be set to <b>NULL</b> if the stream number is not required.

### -param ppIStream [out]

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a> interface of the ASF stream configuration object. The caller must release the interface. This parameter can be <b>NULL</b> if you want to retrieve the stream number without accessing the stream configuration.

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

This method does not create a copy of the stream configuration object. The pointer that is retrieved points to the object within the profile object. You must not make any changes to the stream configuration object using this pointer, because doing so can affect the profile object in unexpected ways.

To change the configuration of the stream configuration object in the profile, you must first clone the stream configuration object by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-clone">IMFASFStreamConfig::Clone</a>. Make whatever changes are required to the clone of the object and then add the updated object by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream">IMFASFProfile::SetStream</a> method.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber">IMFASFProfile::GetStreamByNumber</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount">IMFASFProfile::GetStreamCount</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream">IMFASFProfile::RemoveStream</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream">IMFASFProfile::SetStream</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>