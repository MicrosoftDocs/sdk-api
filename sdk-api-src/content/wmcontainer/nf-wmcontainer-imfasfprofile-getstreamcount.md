---
UID: NF:wmcontainer.IMFASFProfile.GetStreamCount
title: IMFASFProfile::GetStreamCount (wmcontainer.h)
description: Retrieves the number of streams in the profile.
helpviewer_keywords: ["GetStreamCount","GetStreamCount method [Media Foundation]","GetStreamCount method [Media Foundation]","IMFASFProfile interface","IMFASFProfile interface [Media Foundation]","GetStreamCount method","IMFASFProfile.GetStreamCount","IMFASFProfile::GetStreamCount","bf8c6157-3420-4097-8ab6-f307a69d418a","mf.imfasfprofile_getstreamcount","wmcontainer/IMFASFProfile::GetStreamCount"]
old-location: mf\imfasfprofile_getstreamcount.htm
tech.root: mf
ms.assetid: bf8c6157-3420-4097-8ab6-f307a69d418a
ms.date: 12/05/2018
ms.keywords: GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],GetStreamCount method, IMFASFProfile.GetStreamCount, IMFASFProfile::GetStreamCount, bf8c6157-3420-4097-8ab6-f307a69d418a, mf.imfasfprofile_getstreamcount, wmcontainer/IMFASFProfile::GetStreamCount
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
 - IMFASFProfile::GetStreamCount
 - wmcontainer/IMFASFProfile::GetStreamCount
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
 - IMFASFProfile.GetStreamCount
---

# IMFASFProfile::GetStreamCount


## -description

Retrieves the number of streams in the profile.

## -parameters

### -param pcStreams [out]

Receives the number of streams in the profile.

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

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream">IMFASFProfile::GetStream</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream">IMFASFProfile::SetStream</a>