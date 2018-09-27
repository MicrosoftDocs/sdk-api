---
UID: NN:strmif.IAMClockSlave
title: IAMClockSlave
author: windows-sdk-content
description: The IAMClockSlave interface controls the tolerance of an audio renderer when it is matching rates with another clock.If the audio renderer is matching rates with another clock, it allows the audio to drift up to the amount of the specified tolerance.
old-location: dshow\iamclockslave.htm
tech.root: DirectShow
ms.assetid: 7b3d0f93-09dd-4a36-a031-70f61402c314
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAMClockSlave, IAMClockSlave interface [DirectShow], IAMClockSlave interface [DirectShow],described, IAMClockSlaveInterface, dshow.iamclockslave, strmif/IAMClockSlave
ms.prod: windows
ms.technology: windows-sdk
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
 - IAMClockSlave
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMClockSlave interface


## -description



The <code>IAMClockSlave</code> interface controls the tolerance of an audio renderer when it is matching rates with another clock.

If the audio renderer is matching rates with another clock, it allows the audio to drift up to the amount of the specified tolerance. If the audio drifts too far ahead, the renderer drops samples; if it drifts too far behind, the renderer inserts silent gaps. This interface enables an application to change the tolerance from the default.

Setting a larger tolerance is likely to result in the audio stream becoming out of sync with the video stream. Setting a smaller tolerance can cause audio jitter. Therefore, changing the tolerance setting is not recommended, unless you have a specific reason to do so.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMClockSlave</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMClockSlave</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMClockSlave</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a22e17d8-eb96-4e67-bbd7-7c116694c891">GetErrorTolerance</a>
</td>
<td align="left" width="63%">
Retrieves the current tolerance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c93e345-4e4a-4019-9c18-d3d43736fee3">SetErrorTolerance</a>
</td>
<td align="left" width="63%">
Sets the tolerance.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/571fe5e5-9616-463b-837c-f8dbb8adf1be">Live Sources</a>
 

 

