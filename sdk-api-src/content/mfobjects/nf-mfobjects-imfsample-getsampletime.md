---
UID: NF:mfobjects.IMFSample.GetSampleTime
title: IMFSample::GetSampleTime (mfobjects.h)
description: Retrieves the presentation time of the sample.
helpviewer_keywords: ["GetSampleTime","GetSampleTime method [Media Foundation]","GetSampleTime method [Media Foundation]","IMFSample interface","IMFSample interface [Media Foundation]","GetSampleTime method","IMFSample.GetSampleTime","IMFSample::GetSampleTime","fc4aac9e-e7a9-43f0-af7b-54a39666044a","mf.imfsample_getsampletime","mfobjects/IMFSample::GetSampleTime"]
old-location: mf\imfsample_getsampletime.htm
tech.root: mf
ms.assetid: fc4aac9e-e7a9-43f0-af7b-54a39666044a
ms.date: 12/05/2018
ms.keywords: GetSampleTime, GetSampleTime method [Media Foundation], GetSampleTime method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],GetSampleTime method, IMFSample.GetSampleTime, IMFSample::GetSampleTime, fc4aac9e-e7a9-43f0-af7b-54a39666044a, mf.imfsample_getsampletime, mfobjects/IMFSample::GetSampleTime
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
 - IMFSample::GetSampleTime
 - mfobjects/IMFSample::GetSampleTime
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
 - IMFSample.GetSampleTime
---

# IMFSample::GetSampleTime


## -description

Retrieves the presentation time of the sample.

## -parameters

### -param phnsSampleTime [out]

Receives the presentation time, in 100-nanosecond units.

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
<dt><b>MF_E_NO_SAMPLE_TIMESTAMP</b></dt>
</dl>
</td>
<td width="60%">
The sample does not have a presentation time.

</td>
</tr>
</table>

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>