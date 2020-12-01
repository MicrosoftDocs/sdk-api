---
UID: NN:spatialaudioclient.ISpatialAudioObjectRenderStreamBase
title: ISpatialAudioObjectRenderStreamBase (spatialaudioclient.h)
description: Base interface that provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream.
helpviewer_keywords: ["ISpatialAudioObjectRenderStreamBase","ISpatialAudioObjectRenderStreamBase interface [Core Audio]","ISpatialAudioObjectRenderStreamBase interface [Core Audio]","described","coreaudio.ispatialaudioobjectrenderstreambase","spatialaudioclient/ISpatialAudioObjectRenderStreamBase"]
old-location: coreaudio\ispatialaudioobjectrenderstreambase.htm
tech.root: CoreAudio
ms.assetid: 2C2BE871-EFD1-40E1-B466-6BBD09C56852
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamBase, ISpatialAudioObjectRenderStreamBase interface [Core Audio], ISpatialAudioObjectRenderStreamBase interface [Core Audio],described, coreaudio.ispatialaudioobjectrenderstreambase, spatialaudioclient/ISpatialAudioObjectRenderStreamBase
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioObjectRenderStreamBase
 - spatialaudioclient/ISpatialAudioObjectRenderStreamBase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamBase
---

# ISpatialAudioObjectRenderStreamBase interface


## -description

Base interface that provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream. Also provides methods for activating new <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> instances and notifying the system when you are beginning and ending the process of updating activated spatial audio objects and data.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectRenderStreamBase</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioObjectRenderStreamBase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectRenderStreamBase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">BeginUpdatingAudioObjects</a>
</td>
<td align="left" width="63%">
Puts the system into the state where audio object data can be submitted for processing and the <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> state can be modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects">EndUpdatingAudioObjects</a>
</td>
<td align="left" width="63%">
Notifies the system that the app has finished supplying audio data for the spatial audio objects activated with <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ActivateSpatialAudioObject</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-getavailabledynamicobjectcount">GetAvailableDynamicObjectCount</a>
</td>
<td align="left" width="63%">
Gets the number of dynamic spatial audio objects that are currently available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-getservice">GetService</a>
</td>
<td align="left" width="63%">
Gets additional services from the <b>ISpatialAudioObjectRenderStream</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset">Reset</a>
</td>
<td align="left" width="63%">
Reset a stopped audio stream.   
      


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start">Start</a>
</td>
<td align="left" width="63%">
Starts the spatial audio stream.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops a running audio stream.   

</td>
</tr>
</table>