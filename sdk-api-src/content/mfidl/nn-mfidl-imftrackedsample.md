---
UID: NN:mfidl.IMFTrackedSample
title: IMFTrackedSample (mfidl.h)
author: windows-sdk-content
description: Tracks the reference counts on a video media sample.
old-location: mf\imftrackedsample.htm
tech.root: medfound
ms.assetid: 4ad4b14c-94af-4314-8a16-163579dec67f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 4ad4b14c-94af-4314-8a16-163579dec67f, IMFTrackedSample, IMFTrackedSample interface [Media Foundation], IMFTrackedSample interface [Media Foundation],described, mf.imftrackedsample, mfidl/IMFTrackedSample
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFTrackedSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTrackedSample interface


## -description


Tracks the reference counts on a video media sample. Video samples created by the <a href="https://msdn.microsoft.com/d34d423b-4510-44ce-ab46-51560b01f205">MFCreateVideoSampleFromSurface</a> function expose this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTrackedSample</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTrackedSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTrackedSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb9ffeb3-60af-4cef-bbbc-f4be53d48df0">SetAllocator</a>
</td>
<td align="left" width="63%">
Sets the owner for the sample.

</td>
</tr>
</table> 


## -remarks



Use this interface to determine whether it is safe to delete or re-use the buffer contained in a sample. One object assigns itself as the owner of the video sample by calling <a href="https://msdn.microsoft.com/eb9ffeb3-60af-4cef-bbbc-f4be53d48df0">SetAllocator</a>. When all objects release their reference counts on the sample, the owner's callback method is invoked.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

