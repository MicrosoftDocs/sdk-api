---
UID: NF:strmif.IAMAudioInputMixer.put_Loudness
title: IAMAudioInputMixer::put_Loudness (strmif.h)
author: windows-sdk-content
description: The put_Loudness method enables or disables the loudness control.
old-location: dshow\iamaudioinputmixer_put_loudness.htm
tech.root: DirectShow
ms.assetid: e4baca46-260c-45fe-8c03-304c906aab15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Loudness method, IAMAudioInputMixer.put_Loudness, IAMAudioInputMixer::put_Loudness, IAMAudioInputMixerput_Loudness, dshow.iamaudioinputmixer_put_loudness, put_Loudness, put_Loudness method [DirectShow], put_Loudness method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Loudness
ms.topic: method
f1_keywords: 
 - "strmif/IAMAudioInputMixer.put_Loudness"
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
 - IAMAudioInputMixer.put_Loudness
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMAudioInputMixer::put_Loudness


## -description



The <code>put_Loudness</code> method enables or disables the loudness control.




## -parameters




### -param fLoudness [in]

Specifies whether loudness is on or off. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Sets loudness on.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Sets loudness off.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



Loudness boosts the bass of low volume signals before they are recorded, to compensate for the fact that the ear does not hear quiet bass sounds as well as other sounds.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_loudness">IAMAudioInputMixer::get_Loudness</a>
 

 

