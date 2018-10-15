---
UID: NF:mfobjects.IMFSample.SetSampleDuration
title: IMFSample::SetSampleDuration
author: windows-sdk-content
description: Sets the duration of the sample.
old-location: mf\imfsample_setsampleduration.htm
tech.root: medfound
ms.assetid: f97be98e-8f1b-4bae-8cdd-8bdfe107894d
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFSample interface [Media Foundation],SetSampleDuration method, IMFSample.SetSampleDuration, IMFSample::SetSampleDuration, SetSampleDuration, SetSampleDuration method [Media Foundation], SetSampleDuration method [Media Foundation],IMFSample interface, f97be98e-8f1b-4bae-8cdd-8bdfe107894d, mf.imfsample_setsampleduration, mfobjects/IMFSample::SetSampleDuration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSample::SetSampleDuration


## -description



Sets the duration of the sample.




## -parameters




### -param hnsSampleDuration [in]

Duration of the sample, in 100-nanosecond units.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method succeeds if the duration is negative, although negative durations are probably not valid for most types of data. It is the responsibility of the object that consumes the sample to validate the duration.

The duration can also be zero. This might be valid for some types of data. For example, the sample might contain stream metadata with no buffers.

Until this method is called, the <a href="https://msdn.microsoft.com/c3284edc-b9b5-489b-9166-3bb6da50bd2a">IMFSample::GetSampleDuration</a> method returns <b>MF_E_NO_SAMPLE_DURATION</b>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>



<a href="https://msdn.microsoft.com/14389eea-8091-4c10-849e-53db3e98a7c8">Media Samples</a>



<a href="https://msdn.microsoft.com/4ab576ce-becd-4736-921e-e463c0dff841">Time Stamps and Durations</a>
 

 

