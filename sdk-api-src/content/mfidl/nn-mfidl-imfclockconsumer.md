---
UID: NN:mfidl.IMFClockConsumer
title: IMFClockConsumer
author: windows-driver-content
description: Implemented by an app in order to get access to the IMFPresentationClock.
old-location: mf\imfclockconsumer.htm
old-project: medfound
ms.assetid: B21D3797-695F-4794-80A2-05D381F288C2
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFClockConsumer, IMFClockConsumer interface [Media Foundation], IMFClockConsumer interface [Media Foundation], described, mf.imfclockconsumer, mfidl/IMFClockConsumer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFClockConsumer
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFClockConsumer interface


## -description


Implemented by an app in order to get access to the <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFClockConsumer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFClockConsumer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFClockConsumer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92EC184F-EF13-4453-B1C0-D7DCD4C7F44C">GetPresentationClock</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to get an instance of <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F4CC427-1DBE-4586-BA67-7AB472A55408">SetPresentationClock</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to provide the app with an instance of <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>.

</td>
</tr>
</table> 


## -remarks



The media pipeline checks for the presence of this interface by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>. Components can use the presentation clock supplied through this interface to determine how much buffering there is in the pipeline after the component. You can do  this in the <a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">IMFTransform::ProcessInput</a> method by calculating the difference between the value returned by <a href="https://msdn.microsoft.com/31037b75-9fa5-48e0-a58c-a451b445147f">IMFPresentationClock::GetTime</a> and the value returned by <a href="https://msdn.microsoft.com/fc4aac9e-e7a9-43f0-af7b-54a39666044a">IMFSample::GetSampleTime</a>. This difference represents the amount of buffered data after the MFT in the pipeline. 



