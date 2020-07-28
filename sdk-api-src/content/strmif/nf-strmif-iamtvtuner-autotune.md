---
UID: NF:strmif.IAMTVTuner.AutoTune
title: IAMTVTuner::AutoTune (strmif.h)
description: The AutoTune method scans for a precise signal on the channel's frequency.
helpviewer_keywords: ["AutoTune","AutoTune method [DirectShow]","AutoTune method [DirectShow]","IAMTVTuner interface","IAMTVTuner interface [DirectShow]","AutoTune method","IAMTVTuner.AutoTune","IAMTVTuner::AutoTune","IAMTVTunerAutoTune","dshow.iamtvtuner_autotune","strmif/IAMTVTuner::AutoTune"]
old-location: dshow\iamtvtuner_autotune.htm
tech.root: dshow
ms.assetid: ae8338e4-b75d-42d5-bcb7-84352921458c
ms.date: 12/05/2018
ms.keywords: AutoTune, AutoTune method [DirectShow], AutoTune method [DirectShow],IAMTVTuner interface, IAMTVTuner interface [DirectShow],AutoTune method, IAMTVTuner.AutoTune, IAMTVTuner::AutoTune, IAMTVTunerAutoTune, dshow.iamtvtuner_autotune, strmif/IAMTVTuner::AutoTune
f1_keywords:
- strmif/IAMTVTuner.AutoTune
dev_langs:
- c++
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
- IAMTVTuner.AutoTune
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

This method handles the channel-to-frequency conversion and scans for the most precise frequency. Store these values by calling the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-storeautotune">IAMTVTuner::StoreAutoTune</a> method. You can find base frequencies for channels in the appendix <a href="https://docs.microsoft.com/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>
 

 

