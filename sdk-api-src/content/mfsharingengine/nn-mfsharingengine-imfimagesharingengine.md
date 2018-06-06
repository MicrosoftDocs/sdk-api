---
UID: NN:mfsharingengine.IMFImageSharingEngine
title: IMFImageSharingEngine
author: windows-sdk-content
description: Enables image sharing.
old-location: mf\imfimagesharingengine.htm
old-project: medfound
ms.assetid: A30C73DA-9BD5-4D12-A6FB-771BBD2D1191
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFImageSharingEngine, IMFImageSharingEngine interface [Media Foundation], IMFImageSharingEngine interface [Media Foundation],described, mf.imfimagesharingengine, mfsharingengine/IMFImageSharingEngine
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfsharingengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PLAYTO_SOURCE_CREATEFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfsharingengine.h
api_name:
 - IMFImageSharingEngine
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFImageSharingEngine interface


## -description


Enables image sharing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFImageSharingEngine</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFImageSharingEngine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFImageSharingEngine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451305">GetDevice</a>
</td>
<td align="left" width="63%">
Gets information about the image sharing device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59DFAF26-B1D2-4658-B6E8-A0D14F48C734">SetSource</a>
</td>
<td align="left" width="63%">
Sets the source stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the image sharing engine.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

