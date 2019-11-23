---
UID: NF:strmif.IAMTuner.put_Channel
title: IAMTuner::put_Channel (strmif.h)

description: The put_Channel method sets the TV channel.
old-location: dshow\iamtuner_put_channel.htm
tech.root: DirectShow
ms.assetid: 47ad4288-d855-41cd-b8a2-7b3733a87b41

ms.date: 12/05/2018
ms.keywords: IAMTuner interface [DirectShow],put_Channel method, IAMTuner.put_Channel, IAMTuner::put_Channel, IAMTunerput_Channel, dshow.iamtuner_put_channel, put_Channel, put_Channel method [DirectShow], put_Channel method [DirectShow],IAMTuner interface, strmif/IAMTuner::put_Channel
ms.topic: method
f1_keywords: 
 - "strmif/IAMTuner.put_Channel"
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
 - IAMTuner.put_Channel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTuner::put_Channel


## -description



The <code>put_Channel</code> method sets the TV channel.




## -parameters




### -param lChannel [in]

TV channel number.


### -param lVideoSubChannel

Predefined video subchannel value. Specify AMTUNER_SUBCHAN_NO_TUNE for no tuning or AMTUNER_SUBCHAN_DEFAULT for default subchannel. Meaningful only for satellite broadcasts.


### -param lAudioSubChannel

Predefined audio subchannel value. Specify AMTUNER_SUBCHAN_NO_TUNE for no tuning or AMTUNER_SUBCHAN_DEFAULT for default subchannel. Meaningful only for satellite broadcasts.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This method handles the channel-to-frequency function call that converts the TV channel to a TV frequency. For a list of frequencies for channels, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>
 

 

