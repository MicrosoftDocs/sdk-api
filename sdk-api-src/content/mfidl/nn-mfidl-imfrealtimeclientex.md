---
UID: NN:mfidl.IMFRealTimeClientEx
title: IMFRealTimeClientEx (mfidl.h)
author: windows-sdk-content
description: Notifies a pipeline object to register itself with the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\imfrealtimeclientex.htm
tech.root: medfound
ms.assetid: EC5CDD23-B862-4DAE-AC01-4926C4FAD89A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFRealTimeClientEx, IMFRealTimeClientEx interface [Media Foundation], IMFRealTimeClientEx interface [Media Foundation],described, mf.imfrealtimeclientex, mfidl/IMFRealTimeClientEx
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
ms.custom: 19H1
---

# IMFRealTimeClientEx interface


## -description


Notifies a pipeline object to register itself with the Multimedia Class Scheduler Service (MMCSS).



This interface is a replacement for the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient">IMFRealTimeClient</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRealTimeClientEx</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFRealTimeClientEx</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex">RegisterThreadsEx</a>
</td>
<td align="left" width="63%">
Notifies the object to register its worker threads with the Multimedia Class Scheduler Service (MMCSS).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex">SetWorkQueueEx</a>
</td>
<td align="left" width="63%">
Specifies the work queue that this object should use for asynchronous work items. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads">UnregisterThreads</a>
</td>
<td align="left" width="63%">
Notifies the object to unregister its worker threads from the Multimedia Class Scheduler Service (MMCSS).



</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>
 

 

