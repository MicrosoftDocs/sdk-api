---
UID: NF:mfplay.IMFPMediaItem.GetStreamSelection
title: IMFPMediaItem::GetStreamSelection
author: windows-sdk-content
description: Queries whether a stream is selected to play.
old-location: mf\imfpmediaitem_getstreamselection.htm
tech.root: medfound
ms.assetid: 808de13b-123f-4b9c-b2e6-6c0a6f4339fc
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FALSE, GetStreamSelection, GetStreamSelection method [Media Foundation], GetStreamSelection method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetStreamSelection method, IMFPMediaItem.GetStreamSelection, IMFPMediaItem::GetStreamSelection, TRUE, mf.imfpmediaitem_getstreamselection, mfplay/IMFPMediaItem::GetStreamSelection
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
 - IMFPMediaItem.GetStreamSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaItem::GetStreamSelection


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Queries whether a stream is selected to play.


## -parameters




### -param dwStreamIndex [in]

Zero-based index of the stream. To get the number of streams, call <a href="https://msdn.microsoft.com/65a3cfc8-9171-4206-b1b6-54bb0d3ecdd1">IMFPMediaItem::GetNumberOfStreams</a>.


### -param pfEnabled [out]

Receives a Boolean value.

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



To select or deselect a stream, call <a href="https://msdn.microsoft.com/739190a5-60a7-4b50-9919-f68d2cd6da8d">IMFPMediaItem::SetStreamSelection</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

