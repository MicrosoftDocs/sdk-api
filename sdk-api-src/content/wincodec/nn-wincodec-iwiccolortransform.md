---
UID: NN:wincodec.IWICColorTransform
title: IWICColorTransform (wincodec.h)
description: Exposes methods that transforms an IWICBitmapSource from one color context to another.
old-location: wic\_wic_codec_iwiccolortransform.htm
tech.root: wic
ms.assetid: 6c8ae787-3175-4128-ae9f-e11cb0e4c317
ms.date: 12/05/2018
ms.keywords: IWICColorTransform, IWICColorTransform interface [Windows Imaging Component], IWICColorTransform interface [Windows Imaging Component],described, _wic_codec_iwiccolortransform, wic._wic_codec_iwiccolortransform, wincodec/IWICColorTransform
ms.topic: interface
f1_keywords:
- wincodec/IWICColorTransform
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
- IWICColorTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICColorTransform interface


## -description


Exposes methods that transforms an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> from one color context to another.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICColorTransform</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>. <b>IWICColorTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICColorTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccolortransform-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IWICColorTransform</b> with a <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> and transforms it from one <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> to another. 

</td>
</tr>
</table> 


## -remarks



A <b>IWICColorTransform</b> is an imaging pipeline component that knows how to pull pixels obtained from a given <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> through a color transform. The color transform is defined by mapping colors from the source color context to the destination color context in a given output pixel format.

Once initialized, a color transform cannot be reinitialized. Because of this, a color transform cannot be used with multiple sources or varying parameters.



