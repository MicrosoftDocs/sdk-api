---
UID: NF:strmif.IAMTVTuner.get_AudioFrequency
title: IAMTVTuner::get_AudioFrequency
author: windows-sdk-content
description: The get_AudioFrequency method retrieves the currently tuned audio frequency.
old-location: dshow\iamtvtuner_get_audiofrequency.htm
old-project: DirectShow
ms.assetid: 7d0d288a-7ad0-40ad-b86e-9df9447ed484
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAMTVTuner interface [DirectShow],get_AudioFrequency method, IAMTVTuner.get_AudioFrequency, IAMTVTuner::get_AudioFrequency, IAMTVTunerget_AudioFrequency, dshow.iamtvtuner_get_audiofrequency, get_AudioFrequency, get_AudioFrequency method [DirectShow], get_AudioFrequency method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::get_AudioFrequency
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTVTuner.get_AudioFrequency
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTVTuner::get_AudioFrequency


## -description



The <code>get_AudioFrequency</code> method retrieves the currently tuned audio frequency.




## -parameters




### -param lFreq [out]

Pointer to a variable that receives the audio frequency, in hertz (Hz).


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This is a diagnostic method that enables you to examine the exact frequency being used for a given channel.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1c8300c2-be13-4e4c-aa0c-53ce57bc9152">IAMTVTuner Interface</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

