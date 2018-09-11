---
UID: NF:evr.IMFDesiredSample.Clear
title: IMFDesiredSample::Clear
author: windows-sdk-content
description: Clears the time stamps previously set by a call to IMFDesiredSample::SetDesiredSampleTimeAndDuration.
old-location: mf\imfdesiredsample_clear.htm
tech.root: medfound
ms.assetid: d5c6c1c2-c122-47b6-82b3-28b54bafc7b8
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: Clear, Clear method [Media Foundation], Clear method [Media Foundation],IMFDesiredSample interface, IMFDesiredSample interface [Media Foundation],Clear method, IMFDesiredSample.Clear, IMFDesiredSample::Clear, d5c6c1c2-c122-47b6-82b3-28b54bafc7b8, evr/IMFDesiredSample::Clear, mf.imfdesiredsample_clear
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
 - IMFDesiredSample.Clear
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDesiredSample::Clear


## -description



Clears the time stamps previously set by a call to <a href="https://msdn.microsoft.com/12877b24-83ec-4156-b411-f07202fdfd62">IMFDesiredSample::SetDesiredSampleTimeAndDuration</a>.




## -parameters






## -returns



This method does not return a value.




## -remarks



After this method is called, the <a href="https://msdn.microsoft.com/095202ed-0272-4bda-a268-6a407ef74a94">IMFDesiredSample::GetDesiredSampleTimeAndDuration</a> method returns MF_E_NOT_AVAILABLE.

This method also clears the time stamp and duration and removes all attributes from the sample.




## -see-also




<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/373c076c-6329-4332-9f07-f18a01197659">IMFDesiredSample</a>
 

 

