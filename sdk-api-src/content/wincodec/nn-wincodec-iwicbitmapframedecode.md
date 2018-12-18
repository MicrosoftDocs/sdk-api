---
UID: NN:wincodec.IWICBitmapFrameDecode
title: IWICBitmapFrameDecode
author: windows-sdk-content
description: Defines methods for decoding individual image frames of an encoded file.
old-location: wic\_wic_codec_iwicbitmapframedecode.htm
tech.root: wic
ms.assetid: 1498b800-6449-440f-bed7-85891637e559
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWICBitmapFrameDecode, IWICBitmapFrameDecode interface [Windows Imaging Component], IWICBitmapFrameDecode interface [Windows Imaging Component],described, _wic_codec_iwicbitmapframedecode, wic._wic_codec_iwicbitmapframedecode, wincodec/IWICBitmapFrameDecode
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapFrameDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapFrameDecode interface


## -description


Defines methods for decoding individual image frames of an encoded file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapFrameDecode</b> interface inherits from <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>. <b>IWICBitmapFrameDecode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapFrameDecode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b869fc51-0f03-4f93-b5ad-805f9b216423">GetColorContexts</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> associated with the image frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e28de664-f9f1-4cf1-b2a7-f310548a3786">GetMetadataQueryReader</a>
</td>
<td align="left" width="63%">
Retrieves a metadata query reader for the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2792b54b-52d7-4205-a016-246a4dc5451d">GetThumbnail</a>
</td>
<td align="left" width="63%">
Retrieves a small preview of the frame, if supported by the codec.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/ms771770(v=VS.85).aspx">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>



<a href="https://msdn.microsoft.com/a05b496a-bd4c-4065-8060-df0f8930cde7">Windows Imaging Component Overview</a>
 

 

