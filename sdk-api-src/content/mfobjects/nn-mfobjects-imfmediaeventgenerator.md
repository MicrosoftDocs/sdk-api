---
UID: NN:mfobjects.IMFMediaEventGenerator
title: IMFMediaEventGenerator
author: windows-sdk-content
description: Retrieves events from any Media Foundation object that generates events.
old-location: mf\imfmediaeventgenerator.htm
tech.root: medfound
ms.assetid: a37d0840-c896-43a0-b3d1-c2a6aaff1b25
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFMediaEventGenerator, IMFMediaEventGenerator interface [Media Foundation], IMFMediaEventGenerator interface [Media Foundation],described, a37d0840-c896-43a0-b3d1-c2a6aaff1b25, mf.imfmediaeventgenerator, mfobjects/IMFMediaEventGenerator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMFMediaEventGenerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEventGenerator interface


## -description


Retrieves events from any Media Foundation object that generates events.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEventGenerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEventGenerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEventGenerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2afddac-46e9-4928-8b5b-44f3fc7c33d3">BeginGetEvent</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request for the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b38e984-d818-4f69-af28-8b54153faebb">EndGetEvent</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request for the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e78464b5-ec6b-4739-a135-352fa297916a">GetEvent</a>
</td>
<td align="left" width="63%">
Retrieves the next event in the queue. This method is synchronous.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bc33665-1385-41e1-9ad0-991fc93e91c0">QueueEvent</a>
</td>
<td align="left" width="63%">
Puts a new event in the object's queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96a16fd3-10bc-4cd9-967a-ceb92e26ccc8">RemoteBeginGetEvent</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/a2afddac-46e9-4928-8b5b-44f3fc7c33d3">BeginGetEvent</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b793760-546c-43d4-8251-d89d8d7152ad">RemoteEndGetEvent</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/6b38e984-d818-4f69-af28-8b54153faebb">EndGetEvent</a>. (Not used by applications.)

</td>
</tr>
</table> 


## -remarks



An object that supports this interface maintains a queue of events. The client of the object can retrieve the events either synchronously or asynchronously. The synchronous method is <a href="https://msdn.microsoft.com/e78464b5-ec6b-4739-a135-352fa297916a">GetEvent</a>. The asynchronous methods are <a href="https://msdn.microsoft.com/a2afddac-46e9-4928-8b5b-44f3fc7c33d3">BeginGetEvent</a> and <a href="https://msdn.microsoft.com/6b38e984-d818-4f69-af28-8b54153faebb">EndGetEvent</a>.




## -see-also




<a href="https://msdn.microsoft.com/2e003ad4-9fcb-4834-a335-e4969ffd3a00">Media Event Generators</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

