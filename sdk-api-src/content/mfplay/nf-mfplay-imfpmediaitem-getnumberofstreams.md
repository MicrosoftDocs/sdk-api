---
UID: NF:mfplay.IMFPMediaItem.GetNumberOfStreams
title: IMFPMediaItem::GetNumberOfStreams
author: windows-sdk-content
description: Gets the number of streams (audio, video, and other) in the media item.
old-location: mf\imfpmediaitem_getnumberofstreams.htm
tech.root: medfound
ms.assetid: 65a3cfc8-9171-4206-b1b6-54bb0d3ecdd1
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetNumberOfStreams, GetNumberOfStreams method [Media Foundation], GetNumberOfStreams method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetNumberOfStreams method, IMFPMediaItem.GetNumberOfStreams, IMFPMediaItem::GetNumberOfStreams, mf.imfpmediaitem_getnumberofstreams, mfplay/IMFPMediaItem::GetNumberOfStreams
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
 - IMFPMediaItem.GetNumberOfStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaItem::GetNumberOfStreams


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the number of streams (audio, video, and other) in the media item.


## -parameters




### -param pdwStreamCount [out]

Receives the number of streams.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

