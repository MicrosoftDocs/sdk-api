---
UID: NN:mfidl.IMFRealTimeClientEx
title: IMFRealTimeClientEx
author: windows-sdk-content
description: Notifies a pipeline object to register itself with the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\imfrealtimeclientex.htm
tech.root: medfound
ms.assetid: EC5CDD23-B862-4DAE-AC01-4926C4FAD89A
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFRealTimeClientEx, IMFRealTimeClientEx interface [Media Foundation], IMFRealTimeClientEx interface [Media Foundation],described, mf.imfrealtimeclientex, mfidl/IMFRealTimeClientEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - IMFRealTimeClientEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFRealTimeClientEx interface


## -description


Notifies a pipeline object to register itself with the Multimedia Class Scheduler Service (MMCSS).



This interface is a replacement for the <a href="https://msdn.microsoft.com/b1d1901e-dd49-421f-9212-61e32cff411e">IMFRealTimeClient</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRealTimeClientEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFRealTimeClientEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFRealTimeClientEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45E3121A-F6FD-49C7-B147-5317C045DE35">RegisterThreadsEx</a>
</td>
<td align="left" width="63%">
Notifies the object to register its worker threads with the Multimedia Class Scheduler Service (MMCSS).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4F91FD8A-A8B6-4066-A0EB-F764A3BFD8A2">SetWorkQueueEx</a>
</td>
<td align="left" width="63%">
Specifies the work queue that this object should use for asynchronous work items. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ADA3DA3-9FCF-4B8B-8FED-07A6CC5DA7E1">UnregisterThreads</a>
</td>
<td align="left" width="63%">
Notifies the object to unregister its worker threads from the Multimedia Class Scheduler Service (MMCSS).



</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>
 

 

