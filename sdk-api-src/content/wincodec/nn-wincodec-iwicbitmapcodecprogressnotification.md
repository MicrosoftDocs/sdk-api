---
UID: NN:wincodec.IWICBitmapCodecProgressNotification
title: IWICBitmapCodecProgressNotification
author: windows-sdk-content
description: Exposes methods used for progress notification for encoders and decoders.
old-location: wic\_wic_codec_iwicbitmapcodecprogressnotification.htm
tech.root: wic
ms.assetid: 8cf3fbca-0953-4dd7-aa44-3e1924cfd8b0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWICBitmapCodecProgressNotification, IWICBitmapCodecProgressNotification interface [Windows Imaging Component], IWICBitmapCodecProgressNotification interface [Windows Imaging Component],described, _wic_codec_iwicbitmapcodecprogressnotification, wic._wic_codec_iwicbitmapcodecprogressnotification, wincodec/IWICBitmapCodecProgressNotification
ms.prod: windows
ms.technology: windows-sdk
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICBitmapCodecProgressNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapCodecProgressNotification interface


## -description


Exposes methods used for progress notification for encoders and decoders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapCodecProgressNotification</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICBitmapCodecProgressNotification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapCodecProgressNotification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac47178a-f149-4313-8673-ece59e88cfb3">RegisterProgressNotification</a>
</td>
<td align="left" width="63%">
Registers a progress notification callback function.

</td>
</tr>
</table> 


## -remarks



This interface is not supported by the Windows provided codecs.




## -see-also




<a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>



<a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a>



<a href="https://msdn.microsoft.com/cd94e0a1-c275-458e-ae7f-85b703fc660e">IWICProgressCallback</a>



<a href="https://msdn.microsoft.com/10dd9fbe-abff-4fc9-a3a5-7c01ecc10a7f">ProgressNotificationCallback</a>



<b>Reference</b>
 

 

