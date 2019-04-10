---
UID: NN:mfobjects.IMFAsyncCallback
title: IMFAsyncCallback (mfobjects.h)
author: windows-sdk-content
description: Callback interface to notify the application when an asynchronous method completes.
old-location: mf\imfasynccallback.htm
tech.root: medfound
ms.assetid: 7edff985-da59-4cc0-96de-1a92e03a7d41
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 7edff985-da59-4cc0-96de-1a92e03a7d41, IMFAsyncCallback, IMFAsyncCallback interface [Media Foundation], IMFAsyncCallback interface [Media Foundation],described, mf.imfasynccallback, mfobjects/IMFAsyncCallback
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
 - IMFAsyncCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAsyncCallback interface


## -description


Callback interface to notify the application when an asynchronous method completes.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAsyncCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFAsyncCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFAsyncCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/374dd139-d3e7-45d0-a7d3-1187b928ef57">GetParameters</a>
</td>
<td align="left" width="63%">
Provides configuration information to the dispatching thread for a callback

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">Invoke</a>
</td>
<td align="left" width="63%">
Called when an asynchronous operation is completed.

</td>
</tr>
</table> 


## -remarks



For more information about asynchronous methods in Microsoft Media Foundation, see <a href="https://msdn.microsoft.com/ea778eaa-6460-4a93-bd6a-1857ea8b6230">Asynchronous Callback Methods</a>.
      

This interface is also used to perform  a work item in a Media Foundation work-queue. For more information, see <a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>. 

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ea778eaa-6460-4a93-bd6a-1857ea8b6230">Asynchronous Callback Methods</a>



<a href="https://msdn.microsoft.com/28832d50-9b15-4eb0-96f9-2032d4edcaf4">MFInvokeCallback</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

