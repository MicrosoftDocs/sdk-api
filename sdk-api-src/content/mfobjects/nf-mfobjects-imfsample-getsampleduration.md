---
UID: NF:mfobjects.IMFSample.GetSampleDuration
title: IMFSample::GetSampleDuration (mfobjects.h)
description: Retrieves the duration of the sample.
helpviewer_keywords: ["GetSampleDuration","GetSampleDuration method [Media Foundation]","GetSampleDuration method [Media Foundation]","IMFSample interface","IMFSample interface [Media Foundation]","GetSampleDuration method","IMFSample.GetSampleDuration","IMFSample::GetSampleDuration","c3284edc-b9b5-489b-9166-3bb6da50bd2a","mf.imfsample_getsampleduration","mfobjects/IMFSample::GetSampleDuration"]
old-location: mf\imfsample_getsampleduration.htm
tech.root: mf
ms.assetid: c3284edc-b9b5-489b-9166-3bb6da50bd2a
ms.date: 12/05/2018
ms.keywords: GetSampleDuration, GetSampleDuration method [Media Foundation], GetSampleDuration method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],GetSampleDuration method, IMFSample.GetSampleDuration, IMFSample::GetSampleDuration, c3284edc-b9b5-489b-9166-3bb6da50bd2a, mf.imfsample_getsampleduration, mfobjects/IMFSample::GetSampleDuration
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFSample::GetSampleDuration
 - mfobjects/IMFSample::GetSampleDuration
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
 - IMFSample.GetSampleDuration
---

# IMFSample::GetSampleDuration


## -description

Retrieves the duration of the sample.

## -parameters

### -param phnsSampleDuration [out]

Receives the duration, in 100-nanosecond units.

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
<dt><b>MF_E_NO_SAMPLE_DURATION</b></dt>
</dl>
</td>
<td width="60%">
The sample does not have a specified duration.

</td>
</tr>
</table>

## -remarks

If the sample contains more than one buffer, the duration includes the data from all of the buffers.

If the retrieved duration is zero, or if the method returns <b>MF_E_NO_SAMPLE_DURATION</b>, the duration is unknown. In that case, it might be possible to calculate the duration from the media type—for example, by using the video frame rate or the audio sampling rate.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>