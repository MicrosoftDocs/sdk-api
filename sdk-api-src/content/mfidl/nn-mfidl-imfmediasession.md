---
UID: NN:mfidl.IMFMediaSession
title: IMFMediaSession
author: windows-sdk-content
description: Provides playback controls for protected and unprotected content.
old-location: mf\imfmediasession.htm
tech.root: medfound
ms.assetid: feebf891-73fa-4fe6-94ca-3594986fc92d
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFMediaSession, IMFMediaSession interface [Media Foundation], IMFMediaSession interface [Media Foundation],described, feebf891-73fa-4fe6-94ca-3594986fc92d, mf.imfmediasession, mfidl/IMFMediaSession
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFMediaSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSession interface


## -description


Provides playback controls for protected and unprotected content. The Media Session and the protected media path (PMP) session objects expose this interface. This interface is the primary interface that applications use to control the Media Foundation pipeline.

To obtain a pointer to this interface, call <a href="https://msdn.microsoft.com/86b2b5ec-231c-4943-9add-1a5a60e72268">MFCreateMediaSession</a> or <a href="https://msdn.microsoft.com/cb492e68-3d8a-49b2-8c0b-bee8065b53a8">MFCreatePMPMediaSession</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSession</b> interface inherits from <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>. <b>IMFMediaSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcb7e5f1-1095-4766-afed-43ad2279abb4">ClearTopologies</a>
</td>
<td align="left" width="63%">
Clears all of the presentations that are queued for playback in the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ed118ae-7538-4ef6-81fc-b762f709838f">Close</a>
</td>
<td align="left" width="63%">
Closes the Media Session and releases all of the resources it is using.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16444da2-68f2-4d94-8c6f-9e512d51e5e9">GetClock</a>
</td>
<td align="left" width="63%">
Retrieves the Media Session's presentation clock.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6899dbe2-a684-487f-ab56-8631b3d5a033">GetFullTopology</a>
</td>
<td align="left" width="63%">
Gets a topology from the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3534cfb9-23ff-42a6-a3db-b5032d427cf2">GetSessionCapabilities</a>
</td>
<td align="left" width="63%">
Gets the capabilities of the Media Session, based on the current presentation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcc576ba-f8be-4106-a270-756b2abf52d4">Pause</a>
</td>
<td align="left" width="63%">
Pauses the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea5313f0-b0fd-4945-97a2-b3f17937294f">SetTopology</a>
</td>
<td align="left" width="63%">
Sets a topology on the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b9663c2-e32e-4075-b397-59ae01558e15">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the Media Session and releases all the resources used by the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bdec0c0-b042-4e5e-a72b-b15942750ced">Start</a>
</td>
<td align="left" width="63%">
Starts the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cc769cc-24ef-4790-a10e-4aec8fb4fc1f">Stop</a>
</td>
<td align="left" width="63%">
Stops the Media Session.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cdd67082-8153-4f48-abc5-278be82ae082">How to Play Media Files with Media Foundation</a>



<a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

