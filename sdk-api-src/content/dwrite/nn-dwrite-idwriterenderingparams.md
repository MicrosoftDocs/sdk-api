---
UID: NN:dwrite.IDWriteRenderingParams
title: IDWriteRenderingParams
author: windows-sdk-content
description: Represents text rendering settings such as ClearType level, enhanced contrast, and gamma correction for glyph rasterization and filtering.
old-location: directwrite\IDWriteRenderingParams.htm
tech.root: DirectWrite
ms.assetid: 28b118e4-9a63-46cf-8ab7-e1039126405b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteRenderingParams, IDWriteRenderingParams interface [Direct Write], IDWriteRenderingParams interface [Direct Write],described, directwrite.IDWriteRenderingParams, dwrite/IDWriteRenderingParams
ms.topic: interface
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteRenderingParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteRenderingParams interface


## -description


 Represents text rendering settings such as ClearType level, enhanced contrast, and gamma correction for glyph rasterization and filtering.

An application typically obtains a rendering parameters object by calling the <a href="https://msdn.microsoft.com/ddb6839a-9033-423a-a3f0-9352ec03e440">IDWriteFactory::CreateMonitorRenderingParams</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteRenderingParams</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteRenderingParams</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteRenderingParams</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62b2aa39-ca8f-4abd-af10-1c1ca7971dcd">GetClearTypeLevel</a>
</td>
<td align="left" width="63%">
Gets the ClearType level of the rendering parameters object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dabce803-4989-4532-bf96-2f7eb09b29fe">GetEnhancedContrast</a>
</td>
<td align="left" width="63%">
Gets the enhanced contrast property of the rendering parameters object. Valid values are greater than or equal to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f83adfd6-055d-4b73-89a8-e0fe5af0b661">GetGamma</a>
</td>
<td align="left" width="63%">
Gets the gamma value used for gamma correction. Valid values must be
     greater than zero and cannot exceed 256.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/faa727b7-3df6-4ad5-ad1f-1c038ea585c8">GetPixelGeometry</a>
</td>
<td align="left" width="63%">
Gets the pixel geometry of the rendering parameters object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/657360c6-3351-400b-bb41-bcd92de3c48d">GetRenderingMode</a>
</td>
<td align="left" width="63%">
Gets the rendering mode of the rendering parameters object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ddb6839a-9033-423a-a3f0-9352ec03e440">IDWriteFactory::CreateMonitorRenderingParams</a>
 

 

