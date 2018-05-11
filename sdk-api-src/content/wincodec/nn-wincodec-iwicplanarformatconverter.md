---
UID: NN:wincodec.IWICPlanarFormatConverter
title: IWICPlanarFormatConverter
author: windows-driver-content
description: Allows a format converter to be initialized with a planar source.
old-location: wic\iwicplanarformatconverter.htm
old-project: wic
ms.assetid: 07258A07-84AA-4DC2-B2E3-14A43AED5617
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWICPlanarFormatConverter, IWICPlanarFormatConverter interface [Windows Imaging Component], IWICPlanarFormatConverter interface [Windows Imaging Component],described, wic.iwicplanarformatconverter, wincodec/IWICPlanarFormatConverter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICPlanarFormatConverter
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPlanarFormatConverter interface


## -description


Allows a format converter to be initialized with a planar source. You can use QueryInterface to obtain this interface from the Windows provided implementation of <a href="https://msdn.microsoft.com/d558aaa7-5962-424c-9e83-363fba09ad50">IWICFormatConverter</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICPlanarFormatConverter</b> interface inherits from <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>. <b>IWICPlanarFormatConverter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICPlanarFormatConverter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24E68425-3758-4E8E-B3F4-46EE8488E3E1">CanConvert</a>
</td>
<td align="left" width="63%">
Query if the format converter can convert from one format to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a format converter with a planar source, and specifies the interleaved output pixel format.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>
 

 

