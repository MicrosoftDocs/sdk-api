---
UID: NF:strmif.IAMAudioInputMixer.put_MixLevel
title: IAMAudioInputMixer::put_MixLevel
author: windows-sdk-content
description: The put_MixLevel method sets the recording level for this input.
old-location: dshow\iamaudioinputmixer_put_mixlevel.htm
old-project: DirectShow
ms.assetid: 07fd327f-d78b-4fc0-9c6a-69cdaa2bcdf6
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_MixLevel method, IAMAudioInputMixer.put_MixLevel, IAMAudioInputMixer::put_MixLevel, IAMAudioInputMixerput_MixLevel, dshow.iamaudioinputmixer_put_mixlevel, put_MixLevel, put_MixLevel method [DirectShow], put_MixLevel method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_MixLevel
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
 - IAMAudioInputMixer.put_MixLevel
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAudioInputMixer::put_MixLevel


## -description



The <code>put_MixLevel</code> method sets the recording level for this input.




## -parameters




### -param Level [in]

Specifies the recording level. The following values are possible.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>0.0 to 1.0</td>
<td>Zero indicates that the recording level is off; the value 1.0 indicates that the recording level is at full volume. Intermediate values are also allowed.</td>
</tr>
<tr>
<td>AMF_AUTOMATICGAIN</td>
<td>Enable automatic adjustment of the recording level.</td>
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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This filter does not support the AMF_AUTOMATICGAIN flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/bdf8f90b-72a4-4faf-9d08-2634582245f8">IAMAudioInputMixer::get_MixLevel</a>
 

 

