---
UID: NN:windows.media.streaming.ITransportParameters
title: ITransportParameters
author: windows-sdk-content
description: Encapsulates the methods needed to provide information about the current transport-related settings of the DMR. These settings include the current transport state and information about what methods can currently be invoked on the DMR.
old-location: mediastreaming\itransportparameters.htm
tech.root: mediastreaming
ms.assetid: 4D104C4E-18EE-418F-8D99-3E766A5478F6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITransportParameters, ITransportParameters interface [Media Streaming API], ITransportParameters interface [Media Streaming API],described, mediastreaming.itransportparameters, windows/ITransportParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - windows.media.streaming.h
api_name:
 - ITransportParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransportParameters interface


## -description


Encapsulates the methods needed to provide information about the current transport-related settings of the DMR.  These settings include the current transport state and information about what methods can currently be invoked on the DMR.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransportParameters</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITransportParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransportParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7">ActionInformation</a>
</td>
<td align="left" width="63%">
Obtains an <a href="https://msdn.microsoft.com/854C7024-D582-405D-8A5F-C152DE8BE0BE">IMediaRendererActionInformation</a> interface that provides information about which  methods can currently be invoked on the DMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C944EFEC-2B4E-4405-8D33-B6AD8DFBEC4E">TrackInformation</a>
</td>
<td align="left" width="63%">
Obtains a  <a href="https://msdn.microsoft.com/47398d9f-9462-49c1-a02c-985212a07363">TrackInformation</a> structure that provides information about the DMR’s track  parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1DA23EC4-9B52-4E14-86F2-052689EDF5D6">TransportInformation</a>
</td>
<td align="left" width="63%">
Obtains a  <a href="https://msdn.microsoft.com/c91f84f2-e19b-4bfa-862d-fc5e1dc756d4">TransportInformation</a> structure that provides information about the DMR’s transport parameters.

</td>
</tr>
</table> 

