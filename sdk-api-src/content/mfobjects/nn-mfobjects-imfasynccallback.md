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
f1_keywords: 
 - "mfobjects/IMFAsyncCallback"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFAsyncCallback interface


## -description


Callback interface to notify the application when an asynchronous method completes.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAsyncCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFAsyncCallback</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters">GetParameters</a>
</td>
<td align="left" width="63%">
Provides configuration information to the dispatching thread for a callback

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Called when an asynchronous operation is completed.

</td>
</tr>
</table> 


## -remarks



For more information about asynchronous methods in Microsoft Media Foundation, see <a href="https://docs.microsoft.com/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>.
      

This interface is also used to perform  a work item in a Media Foundation work-queue. For more information, see <a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>. 

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback">MFInvokeCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>
 

 

