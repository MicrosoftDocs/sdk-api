---
UID: NN:mfplay.IMFPMediaPlayerCallback
title: IMFPMediaPlayerCallback
author: windows-sdk-content
description: Callback interface for the IMFPMediaPlayer interface.
old-location: mf\imfpmediaplayercallback.htm
old-project: medfound
ms.assetid: 7d9d01bf-861a-4c35-93b1-dbf85cbf0a32
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFPMediaPlayerCallback, IMFPMediaPlayerCallback interface [Media Foundation], IMFPMediaPlayerCallback interface [Media Foundation],described, mf.imfpmediaplayercallback, mfplay/IMFPMediaPlayerCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayerCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaPlayerCallback interface


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Callback interface for the <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> interface.

To set the callback, pass an <b>IMFPMediaPlayerCallback</b> pointer to the <a href="https://msdn.microsoft.com/80c668e2-5e93-4af2-871c-646228e18717">MFPCreateMediaPlayer</a>  function in the  <i>pCallback</i>  parameter. The application implements the <b>IMFPMediaPlayerCallback</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMediaPlayerCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFPMediaPlayerCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMediaPlayerCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">OnMediaPlayerEvent</a>
</td>
<td align="left" width="63%">
Called by the MFPlay player object to notify the application of a playback event.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

