---
UID: NN:directmanipulation.IDirectManipulationFrameInfoProvider
title: IDirectManipulationFrameInfoProvider
author: windows-sdk-content
description: Represents a time-keeping object that measures the latency of the composition infrastructure used by the application and provides this data to Direct Manipulation.
old-location: directmanipulation\idirectmanipulationframeinfoprovider.htm
tech.root: directmanipulation
ms.assetid: 15B7CA2A-DEC3-479B-BD41-38A57037002F
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDirectManipulationFrameInfoProvider, IDirectManipulationFrameInfoProvider interface [Direct Manipulation], IDirectManipulationFrameInfoProvider interface [Direct Manipulation],described, directmanipulation.idirectmanipulationframeinfoprovider, directmanipulation/IDirectManipulationFrameInfoProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - DirectManipulation.h
api_name:
 - IDirectManipulationFrameInfoProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationFrameInfoProvider interface


## -description


Represents a time-keeping object that measures the latency of the composition infrastructure used by the application and provides this data to <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationFrameInfoProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationFrameInfoProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationFrameInfoProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f561b81-241f-4f7a-bb5f-a89faf253c98">GetNextFrameInfo</a>
</td>
<td align="left" width="63%">
Retrieves the composition timing information from the compositor.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

