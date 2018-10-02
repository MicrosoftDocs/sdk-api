---
UID: NN:wincodec.IWICPlanarBitmapSourceTransform
title: IWICPlanarBitmapSourceTransform
author: windows-sdk-content
description: Provides access to planar Y’CbCr pixel formats where pixel components are stored in separate component planes.
old-location: wic\iwicplanarbitmapsourcetransform.htm
tech.root: wic
ms.assetid: AA47F10A-C90A-4DAF-973F-2669D7364CB9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICPlanarBitmapSourceTransform, IWICPlanarBitmapSourceTransform interface [Windows Imaging Component], IWICPlanarBitmapSourceTransform interface [Windows Imaging Component],described, wic.iwicplanarbitmapsourcetransform, wincodec/IWICPlanarBitmapSourceTransform
ms.prod: windows
ms.technology: windows-sdk
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
 - IWICPlanarBitmapSourceTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICPlanarBitmapSourceTransform interface


## -description


Provides access to planar Y’CbCr pixel formats where pixel components are stored in separate component planes.  This interface also allows access to other codec optimizations for flip/rotate, scale, and format conversion to other Y’CbCr planar formats; this is similar to the pre-existing <a href="https://msdn.microsoft.com/f9cc348f-d4f0-4e77-90d6-9ff563a1799c">IWICBitmapSourceTransform</a> interface.

QueryInterface can be used to obtain this interface from the Windows provided implementations of <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a> for the JPEG decoder, <a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a>, <a href="https://msdn.microsoft.com/1fcb19ba-34bd-48c0-9964-0c973c31cacc">IWICBitmapFlipRotator</a>, and <a href="https://msdn.microsoft.com/6c8ae787-3175-4128-ae9f-e11cb0e4c317">IWICColorTransform</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICPlanarBitmapSourceTransform</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICPlanarBitmapSourceTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICPlanarBitmapSourceTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0D6FB12B-B5C5-4A36-93FC-AF96BF03ED01">CopyPixels</a>
</td>
<td align="left" width="63%">
Copies pixels into the destination planes.  Configured by the supplied input parameters.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CB601454-591B-4292-A8BF-EA9D1F060AB3">DoesSupportTransform</a>
</td>
<td align="left" width="63%">
Use this method to determine if a desired planar output is supported and allow the caller to choose an optimized code path if it is.  

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50B89A96-72E8-4771-9109-207F4CDD06CB">JPEG YCbCr Support</a>
 

 

