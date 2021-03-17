---
UID: NF:wmcontainer.IMFASFProfile.RemoveStream
title: IMFASFProfile::RemoveStream (wmcontainer.h)
description: Removes a stream from the Advanced Systems Format (ASF) profile object.
helpviewer_keywords: ["IMFASFProfile interface [Media Foundation]","RemoveStream method","IMFASFProfile.RemoveStream","IMFASFProfile::RemoveStream","RemoveStream","RemoveStream method [Media Foundation]","RemoveStream method [Media Foundation]","IMFASFProfile interface","dfe404d3-66ea-407b-a2e0-caa065f41afe","mf.imfasfprofile_removestream","wmcontainer/IMFASFProfile::RemoveStream"]
old-location: mf\imfasfprofile_removestream.htm
tech.root: mf
ms.assetid: dfe404d3-66ea-407b-a2e0-caa065f41afe
ms.date: 12/05/2018
ms.keywords: IMFASFProfile interface [Media Foundation],RemoveStream method, IMFASFProfile.RemoveStream, IMFASFProfile::RemoveStream, RemoveStream, RemoveStream method [Media Foundation], RemoveStream method [Media Foundation],IMFASFProfile interface, dfe404d3-66ea-407b-a2e0-caa065f41afe, mf.imfasfprofile_removestream, wmcontainer/IMFASFProfile::RemoveStream
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
 - IMFASFProfile::RemoveStream
 - wmcontainer/IMFASFProfile::RemoveStream
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
 - IMFASFProfile.RemoveStream
---

# IMFASFProfile::RemoveStream


## -description

Removes a stream from the Advanced Systems Format (ASF) profile object.

## -parameters

### -param wStreamNumber [in]

Stream number of the stream to remove.

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

After a stream is removed, the ASF profile object reassigns stream indexes so that the index values are sequential starting from zero. Any previously stored stream index numbers are no longer valid after deleting a stream.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream">IMFASFProfile::GetStream</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream">IMFASFProfile::SetStream</a>