---
UID: NN:wincodec.IWICDdsDecoder
title: IWICDdsDecoder (wincodec.h)
author: windows-sdk-content
description: Provides information and functionality specific to the DDS image format.
old-location: wic\iwicddsdecoder.htm
tech.root: wic
ms.assetid: 632D1E7B-9C1D-48FB-95B5-1A295FE99577
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICDdsDecoder, IWICDdsDecoder interface [Windows Imaging Component], IWICDdsDecoder interface [Windows Imaging Component],described, wic.iwicddsdecoder, wincodec/IWICDdsDecoder
ms.topic: interface
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
 - IWICDdsDecoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICDdsDecoder interface


## -description


Provides information and functionality specific to the DDS image format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICDdsDecoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICDdsDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICDdsDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8842FD14-575B-4A81-9598-83A5A67415B7">GetFrame</a>
</td>
<td align="left" width="63%">
Retrieves the specified frame of the DDS image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D4EE39D6-54DC-450D-A430-2996D349BEC6">GetParameters</a>
</td>
<td align="left" width="63%">
Gets DDS-specific data.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the WIC DDS codec. To obtain this interface, create an <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> using the DDS codec and QueryInterface for <b>IWICDdsDecoder</b>.



