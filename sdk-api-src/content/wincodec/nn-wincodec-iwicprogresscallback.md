---
UID: NN:wincodec.IWICProgressCallback
title: IWICProgressCallback (wincodec.h)
description: IWICProgressCallback interface is documented only for compliance; its use is not recommended and may be altered or unavailable in the future. Instead, and use RegisterProgressNotification.
old-location: wic\_wic_codec_iwicprogresscallback.htm
tech.root: wic
ms.assetid: cd94e0a1-c275-458e-ae7f-85b703fc660e
ms.date: 12/05/2018
ms.keywords: IWICProgressCallback, IWICProgressCallback interface [Windows Imaging Component], IWICProgressCallback interface [Windows Imaging Component],described, _wic_codec_iwicprogresscallback, wic._wic_codec_iwicprogresscallback, wincodec/IWICProgressCallback
ms.topic: interface
f1_keywords:
- wincodec/IWICProgressCallback
dev_langs:
- c++
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
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
- IWICProgressCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICProgressCallback interface


## -description


<b>IWICProgressCallback</b> interface is documented only for compliance; its use is not recommended and may be altered or unavailable in the future. Instead, and use <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification">RegisterProgressNotification</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICProgressCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICProgressCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICProgressCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicprogresscallback-notify">Notify</a>
</td>
<td align="left" width="63%"></td>
</tr>
</table> 

