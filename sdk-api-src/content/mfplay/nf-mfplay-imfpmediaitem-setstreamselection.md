---
UID: NF:mfplay.IMFPMediaItem.SetStreamSelection
title: IMFPMediaItem::SetStreamSelection
author: windows-sdk-content
description: Selects or deselects a stream.
old-location: mf\imfpmediaitem_setstreamselection.htm
tech.root: medfound
ms.assetid: 739190a5-60a7-4b50-9919-f68d2cd6da8d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FALSE, IMFPMediaItem interface [Media Foundation],SetStreamSelection method, IMFPMediaItem.SetStreamSelection, IMFPMediaItem::SetStreamSelection, SetStreamSelection, SetStreamSelection method [Media Foundation], SetStreamSelection method [Media Foundation],IMFPMediaItem interface, TRUE, mf.imfpmediaitem_setstreamselection, mfplay/IMFPMediaItem::SetStreamSelection
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
 - IMFPMediaItem.SetStreamSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaItem::SetStreamSelection


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Selects or deselects a stream.


## -parameters




### -param dwStreamIndex [in]

Zero-based index of the stream. To get the number of streams, call <a href="https://msdn.microsoft.com/65a3cfc8-9171-4206-b1b6-54bb0d3ecdd1">IMFPMediaItem::GetNumberOfStreams</a>.


### -param fEnabled [in]

Specify whether to select or deselect the stream.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The stream is selected. During playback, this stream will play.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The stream is not selected. During playback, this stream will not play.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use this method to change which streams are selected. The change goes into effect the next time that <a href="https://msdn.microsoft.com/c792a024-c4f8-4e0b-9720-259d1dc28ee8">IMFPMediaPlayer::SetMediaItem</a> is called with this media item. If the media item is already set on the player, the change does not happen unless you call <b>SetMediaItem</b> again with this media item.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

