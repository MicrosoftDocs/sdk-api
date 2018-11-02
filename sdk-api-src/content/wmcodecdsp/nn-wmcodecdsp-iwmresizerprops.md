---
UID: NN:wmcodecdsp.IWMResizerProps
title: IWMResizerProps
author: windows-sdk-content
description: Sets properties on the video resizer DSP.
old-location: mf\iwmresizerpropsinterface.htm
tech.root: medfound
ms.assetid: 12c26507-c729-4143-a0bd-e043d42744f6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IWMResizerProps, IWMResizerProps interface [Media Foundation], IWMResizerProps interface [Media Foundation],described, codecapi.iwmresizerpropsinterface, mf.iwmresizerprops, mf.iwmresizerpropsinterface, wmcodecdsp/IWMResizerProps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMResizerProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMResizerProps interface


## -description


Sets properties on the video resizer DSP.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMResizerProps</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMResizerProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMResizerProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91c37040-a698-489b-95fd-f3088f62e4c9">GetFullCropRegion</a>
</td>
<td align="left" width="63%">
Retrieves the source and destination rectangles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51a11e24-a4c3-49fb-86ec-17baa1773caf">SetClipRegion</a>
</td>
<td align="left" width="63%">
Sets the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5578b90d-3b18-47a2-b4ae-75a4749f9001">SetFullCropRegion</a>
</td>
<td align="left" width="63%">
Sets the source and destination rectangles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5ce36aa-d46c-4c17-bc8d-4840ea496980">SetInterlaceMode</a>
</td>
<td align="left" width="63%">
Specifies whether the input video stream is interlaced.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64a85094-4247-41d8-9bb6-bdaedba62c19">SetResizerQuality</a>
</td>
<td align="left" width="63%">
Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/4acd6366-1abf-43f3-b6c9-4ea17a335cec">Video Resizer DSP</a>
 

 

