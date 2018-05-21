---
UID: NN:evr.IMFDesiredSample
title: IMFDesiredSample
author: windows-driver-content
description: Enables the presenter for the enhanced video renderer (EVR) to request a specific frame from the video mixer.
old-location: mf\imfdesiredsample.htm
old-project: medfound
ms.assetid: 373c076c-6329-4332-9f07-f18a01197659
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 373c076c-6329-4332-9f07-f18a01197659, IMFDesiredSample, IMFDesiredSample interface [Media Foundation], IMFDesiredSample interface [Media Foundation],described, evr/IMFDesiredSample, mf.imfdesiredsample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: MFVideoMixPrefs
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFDesiredSample
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFDesiredSample interface


## -description


Enables the presenter for the enhanced video renderer (EVR) to request a specific frame from the video mixer.

The sample objects created by the <a href="https://msdn.microsoft.com/d34d423b-4510-44ce-ab46-51560b01f205">MFCreateVideoSampleFromSurface</a> function implement this interface. To retrieve a pointer to this interface, call <b>QueryInterface</b> on the sample.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDesiredSample</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFDesiredSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFDesiredSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Clears the time stamps previously set by a call to <a href="https://msdn.microsoft.com/12877b24-83ec-4156-b411-f07202fdfd62">SetDesiredSampleTimeAndDuration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/095202ed-0272-4bda-a268-6a407ef74a94">GetDesiredSampleTimeAndDuration</a>
</td>
<td align="left" width="63%">
Called by the mixer to get the time and duration of the sample requested by the presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12877b24-83ec-4156-b411-f07202fdfd62">SetDesiredSampleTimeAndDuration</a>
</td>
<td align="left" width="63%">
Called by the presenter to set the time and duration of the sample that it requests from the mixer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

