---
UID: NF:strmif.IAMAudioInputMixer.get_TrebleRange
title: IAMAudioInputMixer::get_TrebleRange
author: windows-sdk-content
description: The get_TrebleRange method retrieves the treble range for this input.
old-location: dshow\iamaudioinputmixer_get_treblerange.htm
tech.root: DirectShow
ms.assetid: 726cbdda-5772-43bc-846f-f7d1672cc56f
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_TrebleRange method, IAMAudioInputMixer.get_TrebleRange, IAMAudioInputMixer::get_TrebleRange, IAMAudioInputMixerget_TrebleRange, dshow.iamaudioinputmixer_get_treblerange, get_TrebleRange, get_TrebleRange method [DirectShow], get_TrebleRange method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_TrebleRange
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
 - IAMAudioInputMixer.get_TrebleRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAudioInputMixer::get_TrebleRange


## -description



The <code>get_TrebleRange</code> method retrieves the treble range for this input.




## -parameters




### -param pRange [out]

Receives the largest valid value for the <a href="https://msdn.microsoft.com/09030c17-14d0-4af2-9e9e-64a536133b64">IAMAudioInputMixer::put_Treble</a>. For example, 6.0 means that any value between –6.0 and 6.0 is valid.


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/09030c17-14d0-4af2-9e9e-64a536133b64">IAMAudioInputMixer::put_Treble</a>
 

 

