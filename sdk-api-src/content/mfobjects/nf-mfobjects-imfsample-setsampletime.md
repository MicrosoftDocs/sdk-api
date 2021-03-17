---
UID: NF:mfobjects.IMFSample.SetSampleTime
title: IMFSample::SetSampleTime (mfobjects.h)
description: Sets the presentation time of the sample.
helpviewer_keywords: ["59d32002-2f5c-4a94-bd09-fd5a2c005ffc","IMFSample interface [Media Foundation]","SetSampleTime method","IMFSample.SetSampleTime","IMFSample::SetSampleTime","SetSampleTime","SetSampleTime method [Media Foundation]","SetSampleTime method [Media Foundation]","IMFSample interface","mf.imfsample_setsampletime","mfobjects/IMFSample::SetSampleTime"]
old-location: mf\imfsample_setsampletime.htm
tech.root: mf
ms.assetid: 59d32002-2f5c-4a94-bd09-fd5a2c005ffc
ms.date: 12/05/2018
ms.keywords: 59d32002-2f5c-4a94-bd09-fd5a2c005ffc, IMFSample interface [Media Foundation],SetSampleTime method, IMFSample.SetSampleTime, IMFSample::SetSampleTime, SetSampleTime, SetSampleTime method [Media Foundation], SetSampleTime method [Media Foundation],IMFSample interface, mf.imfsample_setsampletime, mfobjects/IMFSample::SetSampleTime
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
 - IMFSample::SetSampleTime
 - mfobjects/IMFSample::SetSampleTime
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
 - IMFSample.SetSampleTime
---

# IMFSample::SetSampleTime


## -description

Sets the presentation time of the sample.

## -parameters

### -param hnsSampleTime [in]

The presentation time, in 100-nanosecond units.

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

Some pipeline components require samples that have time stamps. Generally the component that generates the data for the sample also sets the time stamp. The Media Session might modify the time stamps.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>



<a href="/windows/desktop/medfound/time-stamps-and-durations">Time Stamps and Durations</a>