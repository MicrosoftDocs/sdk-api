---
UID: NF:evr.IMFDesiredSample.GetDesiredSampleTimeAndDuration
title: IMFDesiredSample::GetDesiredSampleTimeAndDuration
author: windows-sdk-content
description: Called by the mixer to get the time and duration of the sample requested by the presenter.
old-location: mf\imfdesiredsample_getdesiredsampletimeandduration.htm
old-project: medfound
ms.assetid: 095202ed-0272-4bda-a268-6a407ef74a94
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: 095202ed-0272-4bda-a268-6a407ef74a94, GetDesiredSampleTimeAndDuration, GetDesiredSampleTimeAndDuration method [Media Foundation], GetDesiredSampleTimeAndDuration method [Media Foundation],IMFDesiredSample interface, IMFDesiredSample interface [Media Foundation],GetDesiredSampleTimeAndDuration method, IMFDesiredSample.GetDesiredSampleTimeAndDuration, IMFDesiredSample::GetDesiredSampleTimeAndDuration, evr/IMFDesiredSample::GetDesiredSampleTimeAndDuration, mf.imfdesiredsample_getdesiredsampletimeandduration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: evr.h
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
tech.root: 
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFDesiredSample.GetDesiredSampleTimeAndDuration
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFDesiredSample::GetDesiredSampleTimeAndDuration


## -description



Called by the mixer to get the time and duration of the sample requested by the presenter.




## -parameters




### -param phnsSampleTime [out]

Receives the desired sample time that should be mixed.


### -param phnsSampleDuration [out]

Receives the sample duration that should be mixed.


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
<dt><b>MF_E_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No time stamp was set for this sample. See <a href="https://msdn.microsoft.com/d5c6c1c2-c122-47b6-82b3-28b54bafc7b8">IMFDesiredSample::Clear</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/373c076c-6329-4332-9f07-f18a01197659">IMFDesiredSample</a>
 

 

