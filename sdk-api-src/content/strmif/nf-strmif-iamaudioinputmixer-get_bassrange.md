---
UID: NF:strmif.IAMAudioInputMixer.get_BassRange
title: IAMAudioInputMixer::get_BassRange
author: windows-sdk-content
description: The get_BassRange method retrieves the bass range.
old-location: dshow\iamaudioinputmixer_get_bassrange.htm
old-project: DirectShow
ms.assetid: e0a77f8c-8608-4e16-bc7a-3c90dde2aad8
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_BassRange method, IAMAudioInputMixer.get_BassRange, IAMAudioInputMixer::get_BassRange, IAMAudioInputMixerget_BassRange, dshow.iamaudioinputmixer_get_bassrange, get_BassRange, get_BassRange method [DirectShow], get_BassRange method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_BassRange
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
 - IAMAudioInputMixer.get_BassRange
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAudioInputMixer::get_BassRange


## -description



The <code>get_BassRange</code> method retrieves the bass range.




## -parameters




### -param pRange [out]

Receives the largest valid value for the <a href="https://msdn.microsoft.com/cf752767-826d-487d-ae05-9737765975c8">IAMAudioInputMixer::put_Bass</a> method. For example, 6.0 means that any value between –6.0 and 6.0 is valid.


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/cf752767-826d-487d-ae05-9737765975c8">IAMAudioInputMixer::put_Bass</a>
 

 

