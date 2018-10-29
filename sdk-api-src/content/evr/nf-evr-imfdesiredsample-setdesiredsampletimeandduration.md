---
UID: NF:evr.IMFDesiredSample.SetDesiredSampleTimeAndDuration
title: IMFDesiredSample::SetDesiredSampleTimeAndDuration
author: windows-sdk-content
description: Called by the presenter to set the time and duration of the sample that it requests from the mixer.
old-location: mf\imfdesiredsample_setdesiredsampletimeandduration.htm
tech.root: medfound
ms.assetid: 12877b24-83ec-4156-b411-f07202fdfd62
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 12877b24-83ec-4156-b411-f07202fdfd62, IMFDesiredSample interface [Media Foundation],SetDesiredSampleTimeAndDuration method, IMFDesiredSample.SetDesiredSampleTimeAndDuration, IMFDesiredSample::SetDesiredSampleTimeAndDuration, SetDesiredSampleTimeAndDuration, SetDesiredSampleTimeAndDuration method [Media Foundation], SetDesiredSampleTimeAndDuration method [Media Foundation],IMFDesiredSample interface, evr/IMFDesiredSample::SetDesiredSampleTimeAndDuration, mf.imfdesiredsample_setdesiredsampletimeandduration
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFDesiredSample.SetDesiredSampleTimeAndDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDesiredSample::SetDesiredSampleTimeAndDuration


## -description



Called by the presenter to set the time and duration of the sample that it requests from the mixer.




## -parameters




### -param hnsSampleTime [in]

The time of the requested sample.


### -param hnsSampleDuration [in]

The duration of the requested sample.


## -returns



This method does not return a value.




## -remarks



This value should be set prior to passing the buffer to the mixer for a Mix operation. The mixer sets the actual start and duration times on the sample before sending it back.




## -see-also




<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/373c076c-6329-4332-9f07-f18a01197659">IMFDesiredSample</a>
 

 

