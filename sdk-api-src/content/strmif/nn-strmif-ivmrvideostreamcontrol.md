---
UID: NN:strmif.IVMRVideoStreamControl
title: IVMRVideoStreamControl (strmif.h)
author: windows-sdk-content
description: The IVMRVideoStreamControl interface is implemented on each input pin of the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrvideostreamcontrol.htm
tech.root: DirectShow
ms.assetid: b42fa81e-99d7-4051-b909-2189581825d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRVideoStreamControl, IVMRVideoStreamControl interface [DirectShow], IVMRVideoStreamControl interface [DirectShow],described, IVMRVideoStreamControlInterface, dshow.ivmrvideostreamcontrol, strmif/IVMRVideoStreamControl
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRVideoStreamControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRVideoStreamControl interface


## -description



The <code>IVMRVideoStreamControl</code> interface is implemented on each input pin of the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). The interface operates on the input stream represented by the pin. This interface is used by upstream filters (typically decoders) to get or set the active state of individual streams, or the source color key for the composited image. Applications in general should not use this interface.

The VMR-9 input pins expose the <a href="https://msdn.microsoft.com/df642ebb-058b-41db-95d3-d7d3bf9a6dd0">IVMRVideoStreamControl9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRVideoStreamControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRVideoStreamControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRVideoStreamControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2075ac12-c799-4716-994f-46ff6928e670">GetColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the source color key currently set for this stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/619ba669-c2a0-46fe-9c12-52105b107351">GetStreamActiveState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30a4009c-5da0-4a07-9d4b-7c9047fb6dd8">SetColorKey</a>
</td>
<td align="left" width="63%">
Sets the source color key that the VMR will use when compositing the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/060a95a4-b984-40c6-afe8-136df96c353e">SetStreamActiveState</a>
</td>
<td align="left" width="63%">
Activates or inactivates an input stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

