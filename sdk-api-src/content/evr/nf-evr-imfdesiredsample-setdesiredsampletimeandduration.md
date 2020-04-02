---
UID: NF:evr.IMFDesiredSample.SetDesiredSampleTimeAndDuration
title: IMFDesiredSample::SetDesiredSampleTimeAndDuration (evr.h)
description: Called by the presenter to set the time and duration of the sample that it requests from the mixer.
old-location: mf\imfdesiredsample_setdesiredsampletimeandduration.htm
tech.root: medfound
ms.assetid: 12877b24-83ec-4156-b411-f07202fdfd62
ms.date: 12/05/2018
ms.keywords: 12877b24-83ec-4156-b411-f07202fdfd62, IMFDesiredSample interface [Media Foundation],SetDesiredSampleTimeAndDuration method, IMFDesiredSample.SetDesiredSampleTimeAndDuration, IMFDesiredSample::SetDesiredSampleTimeAndDuration, SetDesiredSampleTimeAndDuration, SetDesiredSampleTimeAndDuration method [Media Foundation], SetDesiredSampleTimeAndDuration method [Media Foundation],IMFDesiredSample interface, evr/IMFDesiredSample::SetDesiredSampleTimeAndDuration, mf.imfdesiredsample_setdesiredsampletimeandduration
f1_keywords:
- evr/IMFDesiredSample.SetDesiredSampleTimeAndDuration
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDesiredSample::SetDesiredSampleTimeAndDuration


## -description



Called by the presenter to set the time and duration of the sample that it requests from the mixer.




## -parameters




### -param hnsSampleTime [in]

The time of the requested sample.


### -param hnsSampleDuration [in]

The duration of the requested sample.


## -remarks



This value should be set prior to passing the buffer to the mixer for a Mix operation. The mixer sets the actual start and duration times on the sample before sending it back.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfdesiredsample">IMFDesiredSample</a>
 

 

