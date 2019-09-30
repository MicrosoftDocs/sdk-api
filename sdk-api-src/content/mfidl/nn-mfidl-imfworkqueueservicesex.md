---
UID: NN:mfidl.IMFWorkQueueServicesEx
title: IMFWorkQueueServicesEx (mfidl.h)
author: windows-sdk-content
description: Extends the IMFWorkQueueServices interface.
old-location: mf\imfworkqueueservicesex.htm
tech.root: medfound
ms.assetid: 12d4f0f4-9a6d-4782-b5ae-4add6608782a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFWorkQueueServicesEx, IMFWorkQueueServicesEx interface [Media Foundation], IMFWorkQueueServicesEx interface [Media Foundation],described, mf.imfworkqueueservicesex, mfidl/IMFWorkQueueServicesEx
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFWorkQueueServicesEx"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFWorkQueueServicesEx interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a> interface.


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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex">BeginRegisterPlatformWorkQueueWithMMCSSEx</a>
</td>
<td align="left" width="63%">
Registers a platform work queue with Multimedia Class Scheduler Service (MMCSS) using the specified
    class and task id.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-getplatformworkqueuemmcsspriority">GetPlatformWorkQueueMMCSSPriority</a>
</td>
<td align="left" width="63%">
Gets the priority of the Multimedia Class Scheduler Service (MMCSS)  priority associated with
    the specified platform work queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-gettopologyworkqueuemmcsspriority">GetTopologyWorkQueueMMCSSPriority</a>
</td>
<td align="left" width="63%">
Retrieves the Multimedia Class Scheduler Service (MMCSS)  string associated with the given topology work queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfworkqueueservicesex-remotebeginregisterplatformworkqueuewithmmcssex">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex">IMFWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx</a>.

</td>
</tr>
</table> 


## -remarks



This interface allows applications to control
both platform and topology work queues.

The <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a> can be obtained from the session by querying     for the <b>MF_WORKQUEUE_SERVICES</b> service.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

