---
UID: NF:evr.IMFDesiredSample.Clear
title: IMFDesiredSample::Clear (evr.h)
description: Clears the time stamps previously set by a call to IMFDesiredSample::SetDesiredSampleTimeAndDuration.
old-location: mf\imfdesiredsample_clear.htm
tech.root: medfound
ms.assetid: d5c6c1c2-c122-47b6-82b3-28b54bafc7b8
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Media Foundation], Clear method [Media Foundation],IMFDesiredSample interface, IMFDesiredSample interface [Media Foundation],Clear method, IMFDesiredSample.Clear, IMFDesiredSample::Clear, d5c6c1c2-c122-47b6-82b3-28b54bafc7b8, evr/IMFDesiredSample::Clear, mf.imfdesiredsample_clear
f1_keywords:
- evr/IMFDesiredSample.Clear
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
- IMFDesiredSample.Clear
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDesiredSample::Clear


## -description



Clears the time stamps previously set by a call to <a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration">IMFDesiredSample::SetDesiredSampleTimeAndDuration</a>.




## -parameters






## -returns



This method does not return a value.




## -remarks



After this method is called, the <a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfdesiredsample-getdesiredsampletimeandduration">IMFDesiredSample::GetDesiredSampleTimeAndDuration</a> method returns MF_E_NOT_AVAILABLE.

This method also clears the time stamp and duration and removes all attributes from the sample.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfdesiredsample">IMFDesiredSample</a>
 

 

