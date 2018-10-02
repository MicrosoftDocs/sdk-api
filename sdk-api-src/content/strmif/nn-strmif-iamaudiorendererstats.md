---
UID: NN:strmif.IAMAudioRendererStats
title: IAMAudioRendererStats
author: windows-sdk-content
description: The IAMAudioRendererStats interface retrieves statistical performance information from an audio renderer filter.This interface is intended for use during development, to log performance data from the audio renderer.
old-location: dshow\iamaudiorendererstats.htm
tech.root: DirectShow
ms.assetid: f5cca658-73ce-4f4d-8992-afb7824f4117
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAMAudioRendererStats, IAMAudioRendererStats interface [DirectShow], IAMAudioRendererStats interface [DirectShow],described, IAMAudioRendererStatsInterface, dshow.iamaudiorendererstats, strmif/IAMAudioRendererStats
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMAudioRendererStats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAudioRendererStats interface


## -description



The <code>IAMAudioRendererStats</code> interface retrieves statistical performance information from an audio renderer filter.

This interface is intended for use during development, to log performance data from the audio renderer. There is probably no reason for an application to use it in a retail build. The <a href="https://msdn.microsoft.com/a3f2776b-974b-4886-82a3-38e00b607a07">Audio Renderer (WaveOut)</a> filter and the <a href="https://msdn.microsoft.com/ec6cc790-8c1f-4de4-a7ca-a7073894380e">DirectSound Renderer</a> filter both expose this interface.

<b>Filter Developers</b>: It is not expected that other filters will implement this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMAudioRendererStats</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMAudioRendererStats</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMAudioRendererStats</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc01cac7-316f-4d18-ae68-c3db4dbf03fa">GetStatParam</a>
</td>
<td align="left" width="63%">
Retrieves performance information from the filter.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

