---
UID: NN:wmcontainer.IMFASFMultiplexer
title: IMFASFMultiplexer
author: windows-sdk-content
description: Provides methods to create Advanced Systems Format (ASF) data packets.
old-location: mf\imfasfmultiplexer.htm
old-project: medfound
ms.assetid: bdb549b5-425b-4f77-b413-723ceb7acd11
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFASFMultiplexer, IMFASFMultiplexer interface [Media Foundation], IMFASFMultiplexer interface [Media Foundation],described, bdb549b5-425b-4f77-b413-723ceb7acd11, mf.imfasfmultiplexer, wmcontainer/IMFASFMultiplexer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmcontainer.h
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
tech.root: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFMultiplexer
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFMultiplexer interface


## -description


Provides methods to create Advanced Systems Format (ASF) data packets. The methods of this interface process input samples into the packets that make up an ASF data section. The ASF multiplexer exposes this interface. To create the ASF multiplexer, call <a href="https://msdn.microsoft.com/4c3ded7e-51ef-4141-98f2-48b318ba9453">MFCreateASFMultiplexer</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFMultiplexer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFASFMultiplexer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFMultiplexer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a106ea5-976a-40df-a554-1b76d9a07286">End</a>
</td>
<td align="left" width="63%">
Collects data from the multiplexer and updates the ASF ContentInfo object to include that information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>
</td>
<td align="left" width="63%">
Signals the multiplexer to process all queued samples. Call this method after passing the last sample to the multiplexer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves flags indicating the configured multiplexer options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39b9f8a0-fb26-4f46-98fd-b4636f8f88c7">GetNextPacket</a>
</td>
<td align="left" width="63%">
Retrieves the next output ASF packet from the multiplexer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56083ceb-3d39-4fda-995a-f91fa0e16853">GetStatistics</a>
</td>
<td align="left" width="63%">
Retrieves multiplexer statistics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the multiplexer with the data from an ASF ContentInfo object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30a693bb-255c-47a4-8102-1543872b0a5e">ProcessSample</a>
</td>
<td align="left" width="63%">
Delivers input samples to the multiplexer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>
</td>
<td align="left" width="63%">
Sets multiplexer options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54aea995-2beb-4c38-a79f-43a539031d95">SetSyncTolerance</a>
</td>
<td align="left" width="63%">
Sets the maximum time by which samples from various streams can be out of synchronization.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/007a6da5-47cf-476a-b0f7-566a68ad19ce">ASF Multiplexer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

