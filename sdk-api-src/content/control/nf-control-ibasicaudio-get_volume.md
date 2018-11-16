---
UID: NF:control.IBasicAudio.get_Volume
title: IBasicAudio::get_Volume
author: windows-sdk-content
description: The get_Volume method retrieves the volume (amplitude) of the audio signal.
old-location: dshow\ibasicaudio_get_volume.htm
tech.root: DirectShow
ms.assetid: 3258da5a-ab44-4c8a-813b-79a0c28693a3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBasicAudio interface [DirectShow],get_Volume method, IBasicAudio.get_Volume, IBasicAudio::get_Volume, IBasicAudioget_Volume, control/IBasicAudio::get_Volume, dshow.ibasicaudio_get_volume, get_Volume, get_Volume method [DirectShow], get_Volume method [DirectShow],IBasicAudio interface
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
 - IBasicAudio.get_Volume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- control.h
: 
- IBasicAudio.get_Volume
: 
---

# IBasicAudio::get_Volume


## -description



The <code>get_Volume</code> method retrieves the volume (amplitude) of the audio signal.




## -parameters




### -param plVolume [out]

Pointer to a variable that receive the volume. Divide by 100 to get equivalent decibel value. For example, –10,000 is –100 dB.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

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
 

 

