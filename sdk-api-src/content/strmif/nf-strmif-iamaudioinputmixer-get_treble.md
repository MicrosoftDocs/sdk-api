---
UID: NF:strmif.IAMAudioInputMixer.get_Treble
title: IAMAudioInputMixer::get_Treble
author: windows-driver-content
description: The get_Treble method retrieves the treble equalization.
old-location: dshow\iamaudioinputmixer_get_treble.htm
old-project: DirectShow
ms.assetid: 6876e121-cb04-49f9-aee4-27759f93529b
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Treble method, IAMAudioInputMixer.get_Treble, IAMAudioInputMixer::get_Treble, IAMAudioInputMixerget_Treble, dshow.iamaudioinputmixer_get_treble, get_Treble, get_Treble method [DirectShow], get_Treble method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Treble
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
-	IAMAudioInputMixer.get_Treble
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAudioInputMixer::get_Treble


## -description



The <code>get_Treble</code> method retrieves the treble equalization.




## -parameters




### -param pTreble [out]

Receives the treble gain, in decibels. A negative value indicates attenuation.


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/09030c17-14d0-4af2-9e9e-64a536133b64">IAMAudioInputMixer::put_Treble</a>
 

 

