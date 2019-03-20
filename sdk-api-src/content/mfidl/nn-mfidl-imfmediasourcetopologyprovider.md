---
UID: NN:mfidl.IMFMediaSourceTopologyProvider
title: IMFMediaSourceTopologyProvider (mfidl.h)
author: windows-sdk-content
description: Enables an application to get a topology from the sequencer source.
old-location: mf\imfmediasourcetopologyprovider.htm
tech.root: medfound
ms.assetid: 7c08fb54-6a78-4b6d-aae7-4b3a823eb880
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 7c08fb54-6a78-4b6d-aae7-4b3a823eb880, IMFMediaSourceTopologyProvider, IMFMediaSourceTopologyProvider interface [Media Foundation], IMFMediaSourceTopologyProvider interface [Media Foundation],described, mf.imfmediasourcetopologyprovider, mfidl/IMFMediaSourceTopologyProvider
ms.topic: interface
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSourceTopologyProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSourceTopologyProvider interface


## -description


Enables an application to get a topology from the sequencer source. This interface is exposed by the sequencer source object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSourceTopologyProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaSourceTopologyProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSourceTopologyProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3889768a-27bb-422e-912b-80546b6017fb">GetMediaSourceTopology</a>
</td>
<td align="left" width="63%">
Returns a topology for a media source that builds an internal topology.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/788ede68-2fd7-45f6-90cb-2426c40f7d4c">Sequencer Source</a>
 

 

