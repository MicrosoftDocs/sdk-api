---
UID: NF:control.IBasicAudio.put_Balance
title: IBasicAudio::put_Balance
author: windows-sdk-content
description: The put_Balance method sets the balance of the audio signal.
old-location: dshow\ibasicaudio_put_balance.htm
old-project: DirectShow
ms.assetid: 88cf4639-8f32-424f-a097-272c44592f6f
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IBasicAudio interface [DirectShow],put_Balance method, IBasicAudio.put_Balance, IBasicAudio::put_Balance, IBasicAudioput_Balance, control/IBasicAudio::put_Balance, dshow.ibasicaudio_put_balance, put_Balance, put_Balance method [DirectShow], put_Balance method [DirectShow],IBasicAudio interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
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
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBasicAudio.put_Balance
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBasicAudio::put_Balance


## -description



The <code>put_Balance</code> method sets the balance of the audio signal.




## -parameters




### -param lBalance [in]

Specifies the balance. The value can range from -10,000 to 10,000. The value -10,000 means the right channel is attenuated by 100 dB and is effectively silent. The value 10,000 means the left channel is silent. The neutral value is 0, which means that both channels are at full volume. When one channel is attenuated, the other remains at full volume.


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
The underlying audio device returned an error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>lBalance</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The filter graph does not contain an audio renderer filter. (Possibly the source does not contain an audio stream.)

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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0335b263-8d32-4690-a606-ba2b3e382680">IBasicAudio Interface</a>
 

 

