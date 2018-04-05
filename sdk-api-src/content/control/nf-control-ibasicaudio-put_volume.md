---
UID: NF:control.IBasicAudio.put_Volume
title: IBasicAudio::put_Volume method
author: windows-driver-content
description: The put_Volume method sets the volume (amplitude) of the audio signal.
old-location: dshow\ibasicaudio_put_volume.htm
old-project: DirectShow
ms.assetid: 95171b87-e558-450b-8a48-f43a19069218
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IBasicAudio, IBasicAudio interface [DirectShow], put_Volume method, IBasicAudio::put_Volume, IBasicAudioput_Volume, control/IBasicAudio::put_Volume, dshow.ibasicaudio_put_volume, put_Volume method [DirectShow], put_Volume method [DirectShow], IBasicAudio interface, put_Volume,IBasicAudio.put_Volume
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IBasicAudio.put_Volume
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBasicAudio::put_Volume method


## -description



The <code>put_Volume</code> method sets the volume (amplitude) of the audio signal.




## -parameters




### -param lVolume [in]

Specifies the volume, as a number from –10,000 to 0, inclusive. Full volume is 0, and –10,000 is silence. Multiply the desired decibel level by 100. For example, –10,000 = –100 dB.


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
The value of <i>lVolume</i> is invalid.

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
 

 

