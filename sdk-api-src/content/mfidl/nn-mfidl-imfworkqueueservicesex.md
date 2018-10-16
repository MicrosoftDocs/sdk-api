---
UID: NN:mfidl.IMFWorkQueueServicesEx
title: IMFWorkQueueServicesEx
author: windows-sdk-content
description: Extends the IMFWorkQueueServices interface.
old-location: mf\imfworkqueueservicesex.htm
tech.root: medfound
ms.assetid: 12d4f0f4-9a6d-4782-b5ae-4add6608782a
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFWorkQueueServicesEx, IMFWorkQueueServicesEx interface [Media Foundation], IMFWorkQueueServicesEx interface [Media Foundation],described, mf.imfworkqueueservicesex, mfidl/IMFWorkQueueServicesEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFWorkQueueServicesEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFWorkQueueServicesEx interface


## -description


Extends the <a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFWorkQueueServicesEx</b> interface inherits from <b>IMFWorkQueueServices</b>. <b>IMFWorkQueueServicesEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFWorkQueueServicesEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/761e0e51-06e9-4b26-b6ad-afeaa7150e64">BeginRegisterPlatformWorkQueueWithMMCSSEx</a>
</td>
<td align="left" width="63%">
Registers a platform work queue with Multimedia Class Scheduler Service (MMCSS) using the specified
    class and task id.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9271439-8785-4743-9e6f-81342af117f8">GetPlatformWorkQueueMMCSSPriority</a>
</td>
<td align="left" width="63%">
Gets the priority of the Multimedia Class Scheduler Service (MMCSS)  priority associated with
    the specified platform work queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5550e53-cbe9-4956-a079-d2a825fd17ef">GetTopologyWorkQueueMMCSSPriority</a>
</td>
<td align="left" width="63%">
Retrieves the Multimedia Class Scheduler Service (MMCSS)  string associated with the given topology work queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75af7ce6-9b74-4d61-b7f2-5d07538f91cf">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/761e0e51-06e9-4b26-b6ad-afeaa7150e64">IMFWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx</a>.

</td>
</tr>
</table> 


## -remarks



This interface allows applications to control
both platform and topology work queues.

The <a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a> can be obtained from the session by querying     for the <b>MF_WORKQUEUE_SERVICES</b> service.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

