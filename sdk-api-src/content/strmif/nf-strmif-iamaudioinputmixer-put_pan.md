---
UID: NF:strmif.IAMAudioInputMixer.put_Pan
title: IAMAudioInputMixer::put_Pan (strmif.h)
description: The put_Pan method sets the pan level.helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","put_Pan method","IAMAudioInputMixer.put_Pan","IAMAudioInputMixer::put_Pan","IAMAudioInputMixerput_Pan","dshow.iamaudioinputmixer_put_pan","put_Pan","put_Pan method [DirectShow]","put_Pan method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::put_Pan"]
old-location: dshow\iamaudioinputmixer_put_pan.htm
tech.root: DirectShow
ms.assetid: eb0528e0-81d0-45a3-831a-8cf3ff1232b6
ms.date: 12/05/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Pan method, IAMAudioInputMixer.put_Pan, IAMAudioInputMixer::put_Pan, IAMAudioInputMixerput_Pan, dshow.iamaudioinputmixer_put_pan, put_Pan, put_Pan method [DirectShow], put_Pan method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Pan
f1_keywords:
- strmif/IAMAudioInputMixer.put_Pan
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
- IAMAudioInputMixer.put_Pan
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMAudioInputMixer::put_Pan


## -description



The <code>put_Pan</code> method sets the pan level.




## -parameters




### -param Pan [in]

Specifies the pan level. Possible values range from –1.0 to 1.0, as follows.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>-1</td>
<td>Full left</td>
</tr>
<tr>
<td>0</td>
<td>Center</td>
</tr>
<tr>
<td>1</td>
<td>Full right</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



In a stereo recording, setting the pan level to -1.0 or 1.0 sends the entire signal to one channel. The other channel records silence. Panning has no effect for a mono recording.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_pan">IAMAudioInputMixer::get_Pan</a>
 

 

