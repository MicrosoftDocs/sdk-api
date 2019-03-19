---
UID: NN:mfidl.IMFQualityManager
title: IMFQualityManager (mfidl.h)
author: windows-sdk-content
description: Adjusts playback quality. This interface is exposed by the quality manager.
old-location: mf\imfqualitymanager.htm
tech.root: medfound
ms.assetid: 66781a1f-7469-4222-9e99-6b1415830f4c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 66781a1f-7469-4222-9e99-6b1415830f4c, IMFQualityManager, IMFQualityManager interface [Media Foundation], IMFQualityManager interface [Media Foundation],described, mf.imfqualitymanager, mfidl/IMFQualityManager
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
 - IMFQualityManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFQualityManager interface


## -description


Adjusts playback quality. This interface is exposed by the quality manager.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFQualityManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFQualityManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFQualityManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b358d98e-7b02-4c58-b556-cfa15436e435">NotifyPresentationClock</a>
</td>
<td align="left" width="63%">
Called when the Media Session selects a presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6e35d03-ca83-4078-bcc1-b9c1d988de01">NotifyProcessInput</a>
</td>
<td align="left" width="63%">
Called when the media processor is about to deliver an input sample to a pipeline component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90596111-6fbc-4249-a696-bd575cb66830">NotifyProcessOutput</a>
</td>
<td align="left" width="63%">
Called after the media processor gets an output sample from a pipeline component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e88a5672-7afd-4d7e-afa9-e92f9803aca7">NotifyQualityEvent</a>
</td>
<td align="left" width="63%">
Called when a pipeline component sends an <a href="https://msdn.microsoft.com/1b4b6a2d-411e-42d1-a44b-bb1928e1c063">MEQualityNotify</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ff6d923-4a83-401a-a0de-0b1a732c31a5">NotifyTopology</a>
</td>
<td align="left" width="63%">
Called when the Media Session is about to start playing a new topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c71bec12-33aa-4156-a052-cf75c80df263">Shutdown</a>
</td>
<td align="left" width="63%">
Called when the Media Session is shutting down.

</td>
</tr>
</table> 


## -remarks



Media Foundation provides a default quality manager that is tuned for playback. Applications can provide a custom quality manager to the Media Session by setting the <a href="https://msdn.microsoft.com/24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a">MF_SESSION_QUALITY_MANAGER</a> attribute when creating the Media Session.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

