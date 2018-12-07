---
UID: NF:mfplay.IMFPMediaPlayer.SetBalance
title: IMFPMediaPlayer::SetBalance
author: windows-sdk-content
description: Sets the audio balance.
old-location: mf\imfpmediaplayer_setbalance.htm
tech.root: medfound
ms.assetid: cb95d037-54b4-4686-b8e6-5b960998d361
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetBalance method, IMFPMediaPlayer.SetBalance, IMFPMediaPlayer::SetBalance, SetBalance, SetBalance method [Media Foundation], SetBalance method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setbalance, mfplay/IMFPMediaPlayer::SetBalance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayer.SetBalance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::SetBalance


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Sets the audio balance.


## -parameters




### -param flBalance [in]

The audio balance. The value can be any number in the following range (inclusive).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>-1.0</b></dt>
</dl>
</td>
<td width="60%">
The left channel is at full volume; the right channel is silent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>+1.0</b></dt>
</dl>
</td>
<td width="60%">
The right channel is at full volume; the left channel is silent.

</td>
</tr>
</table>
 

If the value is zero, the left and right channels are at equal volumes. The default value is zero.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_OUT_OF_RANGE</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>flBalance</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



If you call this method before playback starts, the setting is applied when playback starts.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

