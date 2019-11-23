---
UID: NN:wincodec.IWICFormatConverterInfo
title: IWICFormatConverterInfo (wincodec.h)

description: Exposes methods that provide information about a pixel format converter.
old-location: wic\_wic_codec_iwicformatconverterinfo.htm
tech.root: wic
ms.assetid: e6e2bade-66c1-4994-89b9-68aa038bdc8c

ms.date: 12/05/2018
ms.keywords: IWICFormatConverterInfo, IWICFormatConverterInfo interface [Windows Imaging Component], IWICFormatConverterInfo interface [Windows Imaging Component],described, _wic_codec_iwicformatconverterinfo, wic._wic_codec_iwicformatconverterinfo, wincodec/IWICFormatConverterInfo
ms.topic: interface
f1_keywords: 
 - "wincodec/IWICFormatConverterInfo"
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
 - IWICFormatConverterInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICFormatConverterInfo interface


## -description


Exposes methods that provide information about a pixel format converter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICFormatConverterInfo</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccomponentinfo">IWICComponentInfo</a>. <b>IWICFormatConverterInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICFormatConverterInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicformatconverterinfo-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a> instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicformatconverterinfo-getpixelformats">GetPixelFormats</a>
</td>
<td align="left" width="63%">
Retrieves a list of GUIDs that signify which pixel formats the converter supports.

</td>
</tr>
</table> 

