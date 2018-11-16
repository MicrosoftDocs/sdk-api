---
UID: NF:strmif.IAMAudioInputMixer.get_Loudness
title: IAMAudioInputMixer::get_Loudness
author: windows-sdk-content
description: The get_Loudness method retrieves the loudness control setting.
old-location: dshow\iamaudioinputmixer_get_loudness.htm
tech.root: DirectShow
ms.assetid: 620003c0-401f-4415-a82f-a80e7b32dbd3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Loudness method, IAMAudioInputMixer.get_Loudness, IAMAudioInputMixer::get_Loudness, IAMAudioInputMixerget_Loudness, dshow.iamaudioinputmixer_get_loudness, get_Loudness, get_Loudness method [DirectShow], get_Loudness method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Loudness
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
 - IAMAudioInputMixer.get_Loudness
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
- IAMAudioInputMixer.get_Loudness
: 
---

# IAMAudioInputMixer::get_Loudness


## -description



The <code>get_Loudness</code> method retrieves the loudness control setting.




## -parameters




### -param pfLoudness [out]

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
<td>Loudness is on.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Loudness is off.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/e4baca46-260c-45fe-8c03-304c906aab15">IAMAudioInputMixer::put_Loudness</a>
 

 

