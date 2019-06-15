---
UID: NN:directmanipulation.IDirectManipulationFrameInfoProvider
title: IDirectManipulationFrameInfoProvider (directmanipulation.h)
author: windows-sdk-content
description: Represents a time-keeping object that measures the latency of the composition infrastructure used by the application and provides this data to Direct Manipulation.
old-location: directmanipulation\idirectmanipulationframeinfoprovider.htm
tech.root: directmanipulation
ms.assetid: 15B7CA2A-DEC3-479B-BD41-38A57037002F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectManipulationFrameInfoProvider, IDirectManipulationFrameInfoProvider interface [Direct Manipulation], IDirectManipulationFrameInfoProvider interface [Direct Manipulation],described, directmanipulation.idirectmanipulationframeinfoprovider, directmanipulation/IDirectManipulationFrameInfoProvider
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
ms.custom: 19H1
---

# IDirectManipulationFrameInfoProvider interface


## -description


Represents a time-keeping object that measures the latency of the composition infrastructure used by the application and provides this data to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationFrameInfoProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationFrameInfoProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationframeinfoprovider-getnextframeinfo">GetNextFrameInfo</a>
</td>
<td align="left" width="63%">
Retrieves the composition timing information from the compositor.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
 

 

