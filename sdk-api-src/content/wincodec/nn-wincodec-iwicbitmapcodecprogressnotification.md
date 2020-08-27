---
UID: NN:wincodec.IWICBitmapCodecProgressNotification
title: IWICBitmapCodecProgressNotification (wincodec.h)
description: Exposes methods used for progress notification for encoders and decoders.
helpviewer_keywords: ["IWICBitmapCodecProgressNotification","IWICBitmapCodecProgressNotification interface [Windows Imaging Component]","IWICBitmapCodecProgressNotification interface [Windows Imaging Component]","described","_wic_codec_iwicbitmapcodecprogressnotification","wic._wic_codec_iwicbitmapcodecprogressnotification","wincodec/IWICBitmapCodecProgressNotification"]
old-location: wic\_wic_codec_iwicbitmapcodecprogressnotification.htm
tech.root: wic
ms.assetid: 8cf3fbca-0953-4dd7-aa44-3e1924cfd8b0
ms.date: 12/05/2018
ms.keywords: IWICBitmapCodecProgressNotification, IWICBitmapCodecProgressNotification interface [Windows Imaging Component], IWICBitmapCodecProgressNotification interface [Windows Imaging Component],described, _wic_codec_iwicbitmapcodecprogressnotification, wic._wic_codec_iwicbitmapcodecprogressnotification, wincodec/IWICBitmapCodecProgressNotification
f1_keywords:
- wincodec/IWICBitmapCodecProgressNotification
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapCodecProgressNotification interface


## -description


Exposes methods used for progress notification for encoders and decoders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapCodecProgressNotification</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICBitmapCodecProgressNotification</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification">RegisterProgressNotification</a>
</td>
<td align="left" width="63%">
Registers a progress notification callback function.

</td>
</tr>
</table> 


## -remarks



This interface is not supported by the Windows provided codecs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicprogresscallback">IWICProgressCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nc-wincodec-pfnprogressnotification">ProgressNotificationCallback</a>



<b>Reference</b>
 

 

