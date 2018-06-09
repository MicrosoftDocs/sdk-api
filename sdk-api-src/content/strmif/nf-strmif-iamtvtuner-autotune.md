---
UID: NF:strmif.IAMTVTuner.AutoTune
title: IAMTVTuner::AutoTune
author: windows-sdk-content
description: The AutoTune method scans for a precise signal on the channel's frequency.
old-location: dshow\iamtvtuner_autotune.htm
old-project: DirectShow
ms.assetid: ae8338e4-b75d-42d5-bcb7-84352921458c
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: AutoTune, AutoTune method [DirectShow], AutoTune method [DirectShow],IAMTVTuner interface, IAMTVTuner interface [DirectShow],AutoTune method, IAMTVTuner.AutoTune, IAMTVTuner::AutoTune, IAMTVTunerAutoTune, dshow.iamtvtuner_autotune, strmif/IAMTVTuner::AutoTune
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
 - IAMTVTuner.AutoTune
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTVTuner::AutoTune


## -description



The <code>AutoTune</code> method scans for a precise signal on the channel's frequency.




## -parameters




### -param lChannel [in]

TV channel number.


### -param plFoundSignal [out]

Pointer to a variable indicating whether the channel's frequency was found; nonzero indicates found, zero indicates not found.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



TV channels generally map to a unique frequency depending on regional variances. To avoid interference between multiple transmitters that are assigned the same channel when they are in close geographic proximity, small frequency offsets are introduced at each transmitter. In the United States, this offset ranges up to +/– 26.25 kilohertz (kHz).

This method handles the channel-to-frequency conversion and scans for the most precise frequency. Store these values by calling the <a href="https://msdn.microsoft.com/6e39d757-d8bd-4011-9a67-6bf57b5d820b">IAMTVTuner::StoreAutoTune</a> method. You can find base frequencies for channels in the appendix <a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1c8300c2-be13-4e4c-aa0c-53ce57bc9152">IAMTVTuner Interface</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

