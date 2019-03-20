---
UID: NF:strmif.IAMAudioInputMixer.get_Mono
title: IAMAudioInputMixer::get_Mono (strmif.h)
author: windows-sdk-content
description: The get_Mono method queries whether all channels are combined into a mono signal.
old-location: dshow\iamaudioinputmixer_get_mono.htm
tech.root: DirectShow
ms.assetid: 0c0ce59d-6083-4af2-856b-41a1c9d83295
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Mono method, IAMAudioInputMixer.get_Mono, IAMAudioInputMixer::get_Mono, IAMAudioInputMixerget_Mono, dshow.iamaudioinputmixer_get_mono, get_Mono, get_Mono method [DirectShow], get_Mono method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Mono
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
 - IAMAudioInputMixer.get_Mono
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAudioInputMixer::get_Mono


## -description



The <code>get_Mono</code> method queries whether all channels are combined into a mono signal.




## -parameters




### -param pfMono [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Mono</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Multichannel</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/fb45a1ad-b6d8-4129-97f3-a9c99053c0f0">IAMAudioInputMixer::put_Mono</a>
 

 

