---
UID: NN:spatialaudioclient.ISpatialAudioObjectRenderStreamNotify
title: ISpatialAudioObjectRenderStreamNotify
author: windows-sdk-content
description: Provides notifications for spatial audio clients to respond to changes in the state of an ISpatialAudioObjectRenderStream.
old-location: coreaudio\ispatialaudioobjectrenderstreamnotify.htm
tech.root: CoreAudio
ms.assetid: 3729D985-9040-43AD-A8B0-045509FE2F20
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamNotify, ISpatialAudioObjectRenderStreamNotify interface [Core Audio], ISpatialAudioObjectRenderStreamNotify interface [Core Audio],described, coreaudio.ispatialaudioobjectrenderstreamnotify, spatialaudioclient/ISpatialAudioObjectRenderStreamNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectRenderStreamNotify interface


## -description



Provides notifications for spatial audio clients to respond to changes in the state of an  <a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>. 

You register the object that implements this interface by assigning it to the <i>NotifyObject</i> parameter of the <a href="https://msdn.microsoft.com/6FEC7A70-D12E-4DB9-91DC-A54D5CCF8B57">SpatialAudioClientActivationParams</a> structure passed into the <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a> method. After registering its <b>ISpatialAudioObjectRenderStreamNotify</b> interface, the client receives event notifications in the form of callbacks through the <a href="https://msdn.microsoft.com/BC3F1171-26BC-46D0-8AE2-6BCD2393D617">OnAvailableDynamicObjectCountChange</a> method in the interface.



This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectRenderStreamNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioObjectRenderStreamNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectRenderStreamNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BC3F1171-26BC-46D0-8AE2-6BCD2393D617">OnAvailableDynamicObjectCountChange</a>
</td>
<td align="left" width="63%">
Notifies the spatial audio client when the rendering capacity for an <a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a> is about to change, specifies the time after which the change will occur, and specifies the number of dynamic audio objects that will be available after the change.

</td>
</tr>
</table> 

