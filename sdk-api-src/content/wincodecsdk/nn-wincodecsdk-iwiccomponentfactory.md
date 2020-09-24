---
UID: NN:wincodecsdk.IWICComponentFactory
title: IWICComponentFactory (wincodecsdk.h)
description: Exposes methods that create components used by component developers. This includes metadata readers, writers and other services for use by codec and metadata handler developers.
helpviewer_keywords: ["IWICComponentFactory","IWICComponentFactory interface [Windows Imaging Component]","IWICComponentFactory interface [Windows Imaging Component]","described","_wic_codec_iwiccomponentfactory","wic._wic_codec_iwiccomponentfactory","wincodecsdk/IWICComponentFactory"]
old-location: wic\_wic_codec_iwiccomponentfactory.htm
tech.root: wic
ms.assetid: 7aac7268-8f80-4169-9208-1002ca9703e5
ms.date: 12/05/2018
ms.keywords: IWICComponentFactory, IWICComponentFactory interface [Windows Imaging Component], IWICComponentFactory interface [Windows Imaging Component],described, _wic_codec_iwiccomponentfactory, wic._wic_codec_iwiccomponentfactory, wincodecsdk/IWICComponentFactory
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICComponentFactory
 - wincodecsdk/IWICComponentFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICComponentFactory
---

# IWICComponentFactory interface


## -description

Exposes methods that create components used by component developers. This includes metadata readers, writers and other services for use by codec and metadata handler developers.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICComponentFactory</b> interface inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>. <b>IWICComponentFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICComponentFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag">CreateEncoderPropertyBag</a>
</td>
<td align="left" width="63%">
Creates an encoder property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareader">CreateMetadataReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> based on the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer">CreateMetadataReaderFromContainer</a>
</td>
<td align="left" width="63%">
Creates an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> based on the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriter">CreateMetadataWriter</a>
</td>
<td align="left" width="63%">
Creates an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> based on the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader">CreateMetadataWriterFromReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> from the given <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader">CreateQueryReaderFromBlockReader</a>
</td>
<td align="left" width="63%">
Creates a <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a> from the given <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter">CreateQueryWriterFromBlockWriter</a>
</td>
<td align="left" width="63%">
Creates a <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a> from the given <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a>.

</td>
</tr>
</table>