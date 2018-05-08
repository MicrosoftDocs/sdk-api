---
UID: NF:strmif.IAMTuner.get_Channel
title: IAMTuner::get_Channel
author: windows-driver-content
description: The get_Channel method retrieves the channel to which the tuner is set.
old-location: dshow\iamtuner_get_channel.htm
old-project: DirectShow
ms.assetid: 68c1b6da-4380-4831-b554-bbb2e3e55ef9
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMTVTuner interface [DirectShow],get_Channel method, IAMTVTuner::get_Channel, IAMTuner interface [DirectShow],get_Channel method, IAMTuner.get_Channel, IAMTuner::get_Channel, IAMTunerget_Channel, dshow.iamtuner_get_channel, get_Channel, get_Channel method [DirectShow], get_Channel method [DirectShow],IAMTVTuner interface, get_Channel method [DirectShow],IAMTuner interface, strmif/IAMTVTuner::get_Channel, strmif/IAMTuner::get_Channel
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMTuner.get_Channel
-	IAMTVTuner.get_Channel
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTuner::get_Channel


## -description



The <code>get_Channel</code> method retrieves the channel to which the tuner is set.




## -parameters




### -param plChannel [out]

Pointer to a variable that receives the channel. For frequencies, see <a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>



### -param plVideoSubChannel [out]

Pointer to a variable that receives either the video subchannel, or one of the following flags:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>AMTUNER_SUBCHAN_DEFAULT</td>
<td>Default subchannel</td>
</tr>
<tr>
<td>AMTUNER_SUBCHAN_NO_TUNE</td>
<td>No subchannel tuning</td>
</tr>
</table>
 


### -param plAudioSubChannel [out]

Pointer to a variable that receives either the audio subchannel, or one of the following flags:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>AMTUNER_SUBCHAN_DEFAULT</td>
<td>Default subchannel</td>
</tr>
<tr>
<td>AMTUNER_SUBCHAN_NO_TUNE</td>
<td>No subchannel tuning</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

