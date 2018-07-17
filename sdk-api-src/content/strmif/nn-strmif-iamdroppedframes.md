---
UID: NN:strmif.IAMDroppedFrames
title: IAMDroppedFrames
author: windows-sdk-content
description: The IAMDroppedFrames interface retrieves performance information from a video capture filter, including how many frames were dropped and how many were delivered. Applications can use this interface to determine capture performance at run-time.
old-location: dshow\iamdroppedframes.htm
old-project: DirectShow
ms.assetid: b41c3792-76fe-48e0-b2f5-ca3b0ee4c8ae
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IAMDroppedFrames, IAMDroppedFrames interface [DirectShow], IAMDroppedFrames interface [DirectShow],described, IAMDroppedFramesInterface, dshow.iamdroppedframes, strmif/IAMDroppedFrames
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMDroppedFrames
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMDroppedFrames interface


## -description



The <b>IAMDroppedFrames</b> interface retrieves performance information from a video capture filter, including how many frames were dropped and how many were delivered. Applications can use this interface to determine capture performance at run-time.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMDroppedFrames</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMDroppedFrames</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMDroppedFrames</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49b63a9f-8192-4fce-8cfe-c92bd39ca2b0">GetAverageFrameSize</a>
</td>
<td align="left" width="63%">
Retrieves the average size of the frames that the filter has captured.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4dc9e68-f814-4bb4-88ea-88eea32b2577">GetDroppedInfo</a>
</td>
<td align="left" width="63%">
Retrieves an array of frame numbers that were dropped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7e91efb-0755-4319-ac85-abc6ecdc3e2a">GetNumDropped</a>
</td>
<td align="left" width="63%">
Retrieves the total number of frames that the filter has dropped since it started streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16b26c54-343e-4465-9823-fafeac79bb55">GetNumNotDropped</a>
</td>
<td align="left" width="63%">
Retrieves the total number of frames that the filter has delivered since it started streaming.

</td>
</tr>
</table> 


## -remarks



Some filters that expose this interface do not implement the <a href="https://msdn.microsoft.com/d4dc9e68-f814-4bb4-88ea-88eea32b2577">GetDroppedInfo</a> or <a href="https://msdn.microsoft.com/49b63a9f-8192-4fce-8cfe-c92bd39ca2b0">GetAverageFrameSize</a> method.

For Windows Driver Model (WDM) devices, the <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567806">PROPSETID_VIDCAP_DROPPEDFRAMES</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.

The number of dropped frames is reported by the capture driver. This information is not directly correlated with any particular media sample, so it is not accurate on a per-frame basis, although it should be accurate over time.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

