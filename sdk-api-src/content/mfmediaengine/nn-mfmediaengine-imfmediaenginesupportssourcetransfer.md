---
UID: NN:mfmediaengine.IMFMediaEngineSupportsSourceTransfer
title: IMFMediaEngineSupportsSourceTransfer
author: windows-sdk-content
description: Enables the media source to be transferred between the media engine and the sharing engine for Play To.
old-location: mf\imfmediaenginesupportssourcetransfer.htm
old-project: medfound
ms.assetid: 8784dcc2-52f4-41d9-a0ae-3ea7a736b604
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFMediaEngineSupportsSourceTransfer, IMFMediaEngineSupportsSourceTransfer interface [Media Foundation], IMFMediaEngineSupportsSourceTransfer interface [Media Foundation],described, mf.imfmediaenginesupportssourcetransfer, mfmediaengine/IMFMediaEngineSupportsSourceTransfer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineSupportsSourceTransfer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineSupportsSourceTransfer interface


## -description


Enables the media source to be transferred between  the media engine and the sharing engine for Play To.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineSupportsSourceTransfer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineSupportsSourceTransfer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineSupportsSourceTransfer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db7c17cf-020d-4317-801e-35539e25df49">AttachMediaSource</a>
</td>
<td align="left" width="63%">
Attaches the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a085fc53-91a3-46bb-862c-dde16fb7fa42">DetachMediaSource</a>
</td>
<td align="left" width="63%">
Detaches the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7409a6be-7114-42e2-b878-c68d846106c6">ShouldTransferSource</a>
</td>
<td align="left" width="63%">
Specifies wether or not the source should be transferred.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

