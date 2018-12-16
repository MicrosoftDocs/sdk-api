---
UID: NN:amvideo.IQualProp
title: IQualProp
author: windows-sdk-content
description: The IQualProp interface provides methods for retrieving performance information from video renderers.
old-location: dshow\iqualprop.htm
tech.root: DirectShow
ms.assetid: 428dfb97-0dfa-442c-819e-291e6a58f712
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IQualProp, IQualProp interface [DirectShow], IQualProp interface [DirectShow],described, IQualPropInterface, amvideo/IQualProp, dshow.iqualprop
ms.topic: interface
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IQualProp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQualProp interface


## -description



The <b>IQualProp</b> interface provides methods for retrieving performance information from video renderers. The values returned through the interface are reset each time the filter is stopped. The <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> filter and the <a href="https://msdn.microsoft.com/59332096-bdfe-4208-b99a-1f434652f287">Full Screen Renderer</a> filter expose this interface.

Applications can use this interface to retrieve video performance information. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQualProp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IQualProp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQualProp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376916(v=VS.85).aspx">get_AvgFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the average frame rate achieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376917(v=VS.85).aspx">get_AvgSyncOffset</a>
</td>
<td align="left" width="63%">
Retrieves the average time difference between when a frame was due for rendering and when rendering actually began (this is returned as a value in milliseconds).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376918(v=VS.85).aspx">get_DevSyncOffset</a>
</td>
<td align="left" width="63%">
Retrieves the average time difference between when a frame was due for rendering and when rendering actually began (this is returned as a standard deviation).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376919(v=VS.85).aspx">get_FramesDrawn</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames drawn since streaming started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376920(v=VS.85).aspx">get_FramesDroppedInRenderer</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames dropped by the renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376921(v=VS.85).aspx">get_Jitter</a>
</td>
<td align="left" width="63%">
Gets the jitter (variation in time) between successive frames delivered to the video renderer

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

