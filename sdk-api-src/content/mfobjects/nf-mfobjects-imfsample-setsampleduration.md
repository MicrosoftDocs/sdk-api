---
UID: NF:mfobjects.IMFSample.SetSampleDuration
title: IMFSample::SetSampleDuration (mfobjects.h)
description: Sets the duration of the sample.
helpviewer_keywords: ["IMFSample interface [Media Foundation]","SetSampleDuration method","IMFSample.SetSampleDuration","IMFSample::SetSampleDuration","SetSampleDuration","SetSampleDuration method [Media Foundation]","SetSampleDuration method [Media Foundation]","IMFSample interface","f97be98e-8f1b-4bae-8cdd-8bdfe107894d","mf.imfsample_setsampleduration","mfobjects/IMFSample::SetSampleDuration"]
old-location: mf\imfsample_setsampleduration.htm
tech.root: mf
ms.assetid: f97be98e-8f1b-4bae-8cdd-8bdfe107894d
ms.date: 12/05/2018
ms.keywords: IMFSample interface [Media Foundation],SetSampleDuration method, IMFSample.SetSampleDuration, IMFSample::SetSampleDuration, SetSampleDuration, SetSampleDuration method [Media Foundation], SetSampleDuration method [Media Foundation],IMFSample interface, f97be98e-8f1b-4bae-8cdd-8bdfe107894d, mf.imfsample_setsampleduration, mfobjects/IMFSample::SetSampleDuration
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
 - IMFSample::SetSampleDuration
 - mfobjects/IMFSample::SetSampleDuration
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
 - IMFSample.SetSampleDuration
---

# IMFSample::SetSampleDuration


## -description

Sets the duration of the sample.

## -parameters

### -param hnsSampleDuration [in]

Duration of the sample, in 100-nanosecond units.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method succeeds if the duration is negative, although negative durations are probably not valid for most types of data. It is the responsibility of the object that consumes the sample to validate the duration.

The duration can also be zero. This might be valid for some types of data. For example, the sample might contain stream metadata with no buffers.

Until this method is called, the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration">IMFSample::GetSampleDuration</a> method returns <b>MF_E_NO_SAMPLE_DURATION</b>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>



<a href="/windows/desktop/medfound/time-stamps-and-durations">Time Stamps and Durations</a>