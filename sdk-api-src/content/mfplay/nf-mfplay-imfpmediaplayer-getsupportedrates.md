---
UID: NF:mfplay.IMFPMediaPlayer.GetSupportedRates
title: IMFPMediaPlayer::GetSupportedRates
author: windows-sdk-content
description: Gets the range of supported playback rates.
old-location: mf\imfpmediaplayer_getsupportedrates.htm
tech.root: medfound
ms.assetid: e0e738e4-b8e4-41da-8b74-74ce06f17274
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetSupportedRates, GetSupportedRates method [Media Foundation], GetSupportedRates method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetSupportedRates method, IMFPMediaPlayer.GetSupportedRates, IMFPMediaPlayer::GetSupportedRates, mf.imfpmediaplayer_getsupportedrates, mfplay/IMFPMediaPlayer::GetSupportedRates
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
 - IMFPMediaPlayer.GetSupportedRates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::GetSupportedRates


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the range of supported playback rates.


## -parameters




### -param fForwardDirection [in]

Specify  <b>TRUE</b> to get the playback rates for forward playback. Specify <b>FALSE</b> to get the rates for reverse playback.


### -param pflSlowestRate [out]

Receives the slowest supported rate.


### -param pflFastestRate [out]

Receives the fastest supported rate.


## -returns



This method can return one of these values.

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
<dt><b><b>MF_E_UNSUPPORTED_RATE</b></b></dt>
</dl>
</td>
<td width="60%">
The current media item does not support playback in the requested direction (either forward or reverse).

</td>
</tr>
</table>
 




## -remarks



Playback rates are expressed as a ratio of the current rate to the normal rate. For example, 1.0 indicates normal playback speed, 0.5 indicates half speed, and 2.0 indicates twice speed. Positive values indicate forward playback, and negative values indicate reverse playback.





## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

