---
UID: NF:strmif.IAMAudioInputMixer.get_Loudness
title: IAMAudioInputMixer::get_Loudness (strmif.h)
author: windows-sdk-content
description: The get_Loudness method retrieves the loudness control setting.
old-location: dshow\iamaudioinputmixer_get_loudness.htm
tech.root: DirectShow
ms.assetid: 620003c0-401f-4415-a82f-a80e7b32dbd3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Loudness method, IAMAudioInputMixer.get_Loudness, IAMAudioInputMixer::get_Loudness, IAMAudioInputMixerget_Loudness, dshow.iamaudioinputmixer_get_loudness, get_Loudness, get_Loudness method [DirectShow], get_Loudness method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Loudness
ms.topic: method
f1_keywords: 
 - "strmif/IAMAudioInputMixer.get_Loudness"
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
 - IAMAudioInputMixer.get_Loudness
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_loudness">IAMAudioInputMixer::put_Loudness</a>
 

 

