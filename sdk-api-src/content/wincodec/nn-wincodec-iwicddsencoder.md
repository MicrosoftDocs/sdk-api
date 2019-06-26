---
UID: NN:wincodec.IWICDdsEncoder
title: IWICDdsEncoder (wincodec.h)
author: windows-sdk-content
description: Enables writing DDS format specific information to an encoder.
old-location: wic\iwicddsencoder.htm
tech.root: wic
ms.assetid: DF14309F-7595-4ABE-BB6E-03D2914CC86D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICDdsEncoder, IWICDdsEncoder interface [Windows Imaging Component], IWICDdsEncoder interface [Windows Imaging Component],described, wic.iwicddsencoder, wincodec/IWICDdsEncoder
ms.topic: interface
f1_keywords: 
 - "wincodec/IWICDdsEncoder"
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IWICDdsEncoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICDdsEncoder interface


## -description


Enables writing DDS format specific information to an encoder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICDdsEncoder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICDdsEncoder</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe">CreateNewFrame</a>
</td>
<td align="left" width="63%">
Creates a new frame to encode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-getparameters">GetParameters</a>
</td>
<td align="left" width="63%">
Gets DDS-specific data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters">SetParameters</a>
</td>
<td align="left" width="63%">
Sets DDS-specific data.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the WIC DDS codec. To obtain this interface, create an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a> using the DDS codec and QueryInterface for <b>IWICDdsEncoder</b>.



