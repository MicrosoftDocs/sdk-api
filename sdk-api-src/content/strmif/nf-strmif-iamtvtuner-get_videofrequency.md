---
UID: NF:strmif.IAMTVTuner.get_VideoFrequency
title: IAMTVTuner::get_VideoFrequency
author: windows-sdk-content
description: The get_VideoFrequency method retrieves the current video frequency.
old-location: dshow\iamtvtuner_get_videofrequency.htm
tech.root: DirectShow
ms.assetid: d19552ce-1314-4217-9bd3-72369b4334cf
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAMTVTuner interface [DirectShow],get_VideoFrequency method, IAMTVTuner.get_VideoFrequency, IAMTVTuner::get_VideoFrequency, IAMTVTunerget_VideoFrequency, dshow.iamtvtuner_get_videofrequency, get_VideoFrequency, get_VideoFrequency method [DirectShow], get_VideoFrequency method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::get_VideoFrequency
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTVTuner.get_VideoFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTVTuner::get_VideoFrequency


## -description



The <code>get_VideoFrequency</code> method retrieves the current video frequency.




## -parameters




### -param lFreq [out]

Pointer to a variable that receives the video frequency, in hertz (Hz).


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This is a diagnostic method that enables you to examine the exact frequency being used for a given channel.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1c8300c2-be13-4e4c-aa0c-53ce57bc9152">IAMTVTuner Interface</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

