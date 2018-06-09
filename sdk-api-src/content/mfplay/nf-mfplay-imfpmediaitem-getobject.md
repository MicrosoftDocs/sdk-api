---
UID: NF:mfplay.IMFPMediaItem.GetObject
title: IMFPMediaItem::GetObject
author: windows-sdk-content
description: Gets the object that was used to create the media item.
old-location: mf\imfpmediaitem_getobject.htm
old-project: medfound
ms.assetid: 6a6abc57-149d-4e4b-a29f-7b712d24e6df
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetObject, GetObject method [Media Foundation], GetObject method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetObject method, IMFPMediaItem.GetObject, IMFPMediaItem::GetObject, mf.imfpmediaitem_getobject, mfplay/IMFPMediaItem::GetObject
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
 - IMFPMediaItem.GetObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaItem::GetObject


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the object that was used to create the media item.


## -parameters




### -param ppIUnknown [out]

Receives a pointer to the object's <b>IUnknown</b> interface. The caller must release the interface.


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
The media item was created from a URL, not from an object.

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



The object pointer is set if the application uses <a href="https://msdn.microsoft.com/d647df89-b874-448e-ae41-ee3bcb55521f">IMFPMediaPlayer::CreateMediaItemFromObject</a> to create the media item. Otherwise, <b>GetObject</b> returns  MF_E_NOTFOUND.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

