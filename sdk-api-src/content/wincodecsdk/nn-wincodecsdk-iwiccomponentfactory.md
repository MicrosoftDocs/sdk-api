---
UID: NN:wincodecsdk.IWICComponentFactory
title: IWICComponentFactory
author: windows-driver-content
description: Exposes methods that create components used by component developers. This includes metadata readers, writers and other services for use by codec and metadata handler developers.
old-location: wic\_wic_codec_iwiccomponentfactory.htm
old-project: wic
ms.assetid: 7aac7268-8f80-4169-9208-1002ca9703e5
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IWICComponentFactory, IWICComponentFactory interface [Windows Imaging Component], IWICComponentFactory interface [Windows Imaging Component],described, _wic_codec_iwiccomponentfactory, wic._wic_codec_iwiccomponentfactory, wincodecsdk/IWICComponentFactory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICPersistOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICComponentFactory
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICComponentFactory interface


## -description


Exposes methods that create components used by component developers. This includes metadata readers, writers and other services for use by codec and metadata handler developers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICComponentFactory</b> interface inherits from <a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>. <b>IWICComponentFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9d3c801d-46d4-4272-8bd6-9bc196e1b187">CreateEncoderPropertyBag</a>
</td>
<td align="left" width="63%">
Creates an encoder property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fc94831-1743-4269-97af-48116e2a4e1a">CreateMetadataReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a> based on the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/876d2d5a-8247-4e4a-b402-0ee02d9b0158">CreateMetadataReaderFromContainer</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a> based on the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4e82125-bdaa-44c5-a370-22390764753b">CreateMetadataWriter</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a> based on the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f321483c-186b-4405-84f6-f58fddf6b60f">CreateMetadataWriterFromReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a> from the given <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/638d7c29-9c13-4a4b-ac60-8bccd01c65d5">CreateQueryReaderFromBlockReader</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a> from the given <a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ad15754-c180-43e0-a307-6ff84f7eebd6">CreateQueryWriterFromBlockWriter</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a> from the given <a href="https://msdn.microsoft.com/d8e44c64-dd58-4d36-8add-0a0b2e2af5a4">IWICMetadataBlockWriter</a>.

</td>
</tr>
</table> 

