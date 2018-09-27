---
UID: NN:evr.IMFVideoRenderer
title: IMFVideoRenderer
author: windows-sdk-content
description: Sets a new mixer or presenter for the Enhanced Video Renderer (EVR).
old-location: mf\imfvideorenderer.htm
tech.root: medfound
ms.assetid: 70596630-5131-460f-9cb3-adcea201c3b2
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 70596630-5131-460f-9cb3-adcea201c3b2, IMFVideoRenderer, IMFVideoRenderer interface [Media Foundation], IMFVideoRenderer interface [Media Foundation],described, evr/IMFVideoRenderer, mf.imfvideorenderer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: evr.h
req.include-header: 
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoRenderer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoRenderer interface


## -description


Sets a new mixer or presenter for the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR).

Both the EVR media sink and the DirectShow EVR filter implement this interface. To get a pointer to the interface, call <b>QueryInterface</b> on the media sink or the filter. Do not use <a href="https://msdn.microsoft.com/102a1dff-8419-4f86-a145-53ce3d0123f5">IMFGetService</a> to get a pointer to this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoRenderer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e46a9596-9f3f-4430-8d45-bbc9c240be3b">InitializeRenderer</a>
</td>
<td align="left" width="63%">
Sets a new mixer or presenter for the enhanced video renderer (EVR).

</td>
</tr>
</table> 


## -remarks



The EVR activation object returned by the <a href="https://msdn.microsoft.com/021887fc-36af-42d4-ae46-2edc1c700110">MFCreateVideoRendererActivate</a> function does not expose this interface. Instead, the activation object supports attributes that specify a custom mixer or presenter. For more information, see <a href="https://msdn.microsoft.com/33f9bb09-625f-4bbb-a884-70c6bba3700b">Enhanced Video Renderer Attributes</a>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

