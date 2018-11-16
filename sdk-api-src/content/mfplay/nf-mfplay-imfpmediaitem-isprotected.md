---
UID: NF:mfplay.IMFPMediaItem.IsProtected
title: IMFPMediaItem::IsProtected
author: windows-sdk-content
description: Queries whether the media item contains protected content.
old-location: mf\imfpmediaitem_isprotected.htm
tech.root: medfound
ms.assetid: e4ae8b5e-7657-476c-83f9-c27de858e328
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FALSE, IMFPMediaItem interface [Media Foundation],IsProtected method, IMFPMediaItem.IsProtected, IMFPMediaItem::IsProtected, IsProtected, IsProtected method [Media Foundation], IsProtected method [Media Foundation],IMFPMediaItem interface, TRUE, mf.imfpmediaitem_isprotected, mfplay/IMFPMediaItem::IsProtected
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
 - IMFPMediaItem.IsProtected
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfplay.h
: 
- IMFPMediaItem.IsProtected
: 
---

# IMFPMediaItem::IsProtected


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Queries whether the media item contains protected content.
<div class="alert"><b>Note</b>  Currently <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> does not support playing protected content.</div><div> </div>

## -parameters




### -param pfProtected [out]

Receives one of the following values.

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
The media item contains protected content. Attempting to play this media item will cause a playback error.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The media item does not contain protected content.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

