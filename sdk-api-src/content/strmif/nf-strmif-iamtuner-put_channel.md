---
UID: NF:strmif.IAMTuner.put_Channel
title: IAMTuner::put_Channel
author: windows-sdk-content
description: The put_Channel method sets the TV channel.
old-location: dshow\iamtuner_put_channel.htm
tech.root: DirectShow
ms.assetid: 47ad4288-d855-41cd-b8a2-7b3733a87b41
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAMTuner interface [DirectShow],put_Channel method, IAMTuner.put_Channel, IAMTuner::put_Channel, IAMTunerput_Channel, dshow.iamtuner_put_channel, put_Channel, put_Channel method [DirectShow], put_Channel method [DirectShow],IAMTuner interface, strmif/IAMTuner::put_Channel
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
 - IAMTuner.put_Channel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IAMTuner.put_Channel
: 
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



This method handles the channel-to-frequency function call that converts the TV channel to a TV frequency. For a list of frequencies for channels, see <a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

