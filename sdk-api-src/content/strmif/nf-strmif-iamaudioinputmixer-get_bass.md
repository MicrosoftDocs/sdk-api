---
UID: NF:strmif.IAMAudioInputMixer.get_Bass
title: IAMAudioInputMixer::get_Bass
author: windows-sdk-content
description: The get_Bass method retrieves the bass equalization.
old-location: dshow\iamaudioinputmixer_get_bass.htm
tech.root: DirectShow
ms.assetid: 08edf6be-81b7-4402-a500-1b7d9c389042
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Bass method, IAMAudioInputMixer.get_Bass, IAMAudioInputMixer::get_Bass, IAMAudioInputMixerget_Bass, dshow.iamaudioinputmixer_get_bass, get_Bass, get_Bass method [DirectShow], get_Bass method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Bass
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
 - IAMAudioInputMixer.get_Bass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAudioInputMixer::get_Bass


## -description



The <code>get_Bass</code> method retrieves the bass equalization.




## -parameters




### -param pBass [out]

Receives the bass gain, in decibels. A negative value indicates attenuation.


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/cf752767-826d-487d-ae05-9737765975c8">IAMAudioInputMixer::put_Bass</a>
 

 

