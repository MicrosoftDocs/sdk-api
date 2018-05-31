---
UID: NN:strmif.IMediaSample2Config
title: IMediaSample2Config
author: windows-sdk-content
description: The IMediaSample2Config interface returns a pointer to a Direct3D surface representing a VRAM capture buffer.
old-location: dshow\imediasample2config.htm
old-project: DirectShow
ms.assetid: 99a3d957-b504-4242-87de-54b5468f00b5
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMediaSample2Config, IMediaSample2Config interface [DirectShow], IMediaSample2Config interface [DirectShow],described, IMediaSample2ConfigInterface, dshow.imediasample2config, strmif/IMediaSample2Config
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaSample2Config
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSample2Config interface


## -description


The <b>IMediaSample2Config</b> interface returns a pointer to a Direct3D surface representing a VRAM capture buffer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaSample2Config</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaSample2Config</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaSample2Config</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c53306ec-cb5c-4f55-afb0-de72386a166d">GetSurface</a>
</td>
<td align="left" width="63%">
Returns a pointer to the Direct3D surface managed by this media sample.

</td>
</tr>
</table> 


## -remarks



If a display driver supports VRAM capture, the KsProxy filter allocates samples that expose this interface. Downstream filters can use this interface to access the video data in video memory, without requiring the data to be copied into system memory. The display driver must support the Windows Vista Display Driver Model (WDDM).




## -see-also




<a href="https://msdn.microsoft.com/57ee86b0-50bc-4992-94d4-f290f83d2afc">Using WDDM Capture in DirectShow</a>
 

 

