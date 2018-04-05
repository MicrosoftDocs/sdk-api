---
UID: NN:wincodec.IWICDdsEncoder
title: IWICDdsEncoder
author: windows-driver-content
description: Enables writing DDS format specific information to an encoder.
old-location: wic\iwicddsencoder.htm
old-project: wic
ms.assetid: DF14309F-7595-4ABE-BB6E-03D2914CC86D
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IWICDdsEncoder, IWICDdsEncoder interface [Windows Imaging Component], IWICDdsEncoder interface [Windows Imaging Component], described, wic.iwicddsencoder, wincodec/IWICDdsEncoder
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
-	IWICDdsEncoder
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDdsEncoder interface


## -description


Enables writing DDS format specific information to an encoder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICDdsEncoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICDdsEncoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICDdsEncoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14195781-DA71-400A-B4A7-F336A0B5429B">CreateNewFrame</a>
</td>
<td align="left" width="63%">
Creates a new frame to encode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff548095">GetParameters</a>
</td>
<td align="left" width="63%">
Gets DDS-specific data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9DF51D95-97B0-4EC9-8F77-E49B16D76D77">SetParameters</a>
</td>
<td align="left" width="63%">
Sets DDS-specific data.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the WIC DDS codec. To obtain this interface, create an <a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a> using the DDS codec and QueryInterface for <b>IWICDdsEncoder</b>.



