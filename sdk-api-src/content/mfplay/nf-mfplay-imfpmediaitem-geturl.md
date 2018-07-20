---
UID: NF:mfplay.IMFPMediaItem.GetURL
title: IMFPMediaItem::GetURL
author: windows-sdk-content
description: Gets the URL that was used to create the media item.
old-location: mf\imfpmediaitem_geturl.htm
old-project: medfound
ms.assetid: 2598534c-28cc-4f4c-bf87-17ab7044e0c1
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetURL, GetURL method [Media Foundation], GetURL method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetURL method, IMFPMediaItem.GetURL, IMFPMediaItem::GetURL, mf.imfpmediaitem_geturl, mfplay/IMFPMediaItem::GetURL
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFPMediaItem.GetURL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaItem::GetURL


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the URL that was used to create the media item.


## -parameters




### -param ppwszURL [out]

Receives a pointer to a null-terminated string that contains the URL. The caller must free the string by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
No URL is associated with this media item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/c56b07b5-f595-4933-9af6-868fc8938849">IMFPMediaPlayer::Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



This method applies when the application calls  <a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">IMFPMediaPlayer::CreateMediaItemFromURL</a> to create a media item. If the application calls <a href="https://msdn.microsoft.com/d647df89-b874-448e-ae41-ee3bcb55521f">IMFPMediaPlayer::CreateMediaItemFromObject</a> to create a media item, the  <b>GetURL</b> method for that media item returns  <b>MF_E_NOTFOUND</b>.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">IMFPMediaPlayer::CreateMediaItemFromURL</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

