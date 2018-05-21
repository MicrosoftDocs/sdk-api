---
UID: NF:mfplay.IMFPMediaPlayer.GetBalance
title: IMFPMediaPlayer::GetBalance
author: windows-driver-content
description: Gets the current audio balance.
old-location: mf\imfpmediaplayer_getbalance.htm
old-project: medfound
ms.assetid: 27deeb41-5347-4a6d-bfd4-4e4444540651
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: GetBalance, GetBalance method [Media Foundation], GetBalance method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetBalance method, IMFPMediaPlayer.GetBalance, IMFPMediaPlayer::GetBalance, mf.imfpmediaplayer_getbalance, mfplay/IMFPMediaPlayer::GetBalance
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
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplay.h
api_name:
-	IMFPMediaPlayer.GetBalance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaPlayer::GetBalance


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the current audio balance.


## -parameters




### -param pflBalance [out]

Receives the balance. The value can be any number in the following range (inclusive).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1.0</dt>
</dl>
</td>
<td width="60%">
The left channel is at full volume; the right channel is silent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>+1.0</dt>
</dl>
</td>
<td width="60%">
The right channel is at full volume; the left channel is silent.

</td>
</tr>
</table>
 

If the value is zero, the left and right channels are at equal volumes. The default value is zero.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

