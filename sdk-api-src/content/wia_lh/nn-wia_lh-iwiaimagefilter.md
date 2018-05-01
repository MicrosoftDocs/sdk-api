---
UID: NN:wia_lh.IWiaImageFilter
title: IWiaImageFilter
author: windows-driver-content
description: The IWiaImageFilter interface is an extension interface implemented by image processing filter developers and called by Microsoft Windows Image Acquisition (WIA).
old-location: image\iwiaimagefilter_interface.htm
old-project: image
ms.assetid: de74898b-ac04-468d-874d-7ca281e22a86
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaErrorHandler_3922a578-25ee-448c-a0db-c339711ad2cb.xml, IWiaImageFilter, IWiaImageFilter interface [Imaging Devices], IWiaImageFilter interface [Imaging Devices], described, image.iwiaimagefilter_interface, wia_lh/IWiaImageFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wia_lh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wia_lh.h
api_name:
-	IWiaImageFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaImageFilter interface


## -description


The <b>IWiaImageFilter</b> interface is an extension interface implemented by image processing filter developers and called by Microsoft Windows Image Acquisition (WIA).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaImageFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaImageFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaImageFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543912">IWiaImageFilter::FilterPreviewImage</a>
</td>
<td align="left" width="63%">
The <b>IWiaImageFilter::FilterPreviewImage</b> method is called by the WIA Preview component, when an application calls the <b>IWiaPreview::UpdatePreview</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543916">IWiaImageFilter::InitializeFilter</a>
</td>
<td align="left" width="63%">
The <b>IWiaImageFilter::InitializeFilter</b> method stores the references to <i>pWiaItem2</i> and <i>pWiaTransferCallback</i> parameters passed into the method.

</td>
</tr>
</table> 

