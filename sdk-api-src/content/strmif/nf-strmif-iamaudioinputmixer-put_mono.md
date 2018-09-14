---
UID: NF:strmif.IAMAudioInputMixer.put_Mono
title: IAMAudioInputMixer::put_Mono
author: windows-sdk-content
description: The put_Mono method combines all channels into a mono signal.
old-location: dshow\iamaudioinputmixer_put_mono.htm
tech.root: DirectShow
ms.assetid: fb45a1ad-b6d8-4129-97f3-a9c99053c0f0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Mono method, IAMAudioInputMixer.put_Mono, IAMAudioInputMixer::put_Mono, IAMAudioInputMixerput_Mono, dshow.iamaudioinputmixer_put_mono, put_Mono, put_Mono method [DirectShow], put_Mono method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Mono
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
 - IAMAudioInputMixer.put_Mono
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAudioInputMixer::put_Mono


## -description



The <code>put_Mono</code> method combines all channels into a mono signal.




## -parameters




### -param fMono [in]

Specifies mono or multichannel. Use one of the following values.

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



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Error setting mono control.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



In mono mode, a stereo recording of this input will have the same data in both channels. The result will be a mixture of the left and right signals.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/0c0ce59d-6083-4af2-856b-41a1c9d83295">IAMAudioInputMixer::get_Mono</a>
 

 

