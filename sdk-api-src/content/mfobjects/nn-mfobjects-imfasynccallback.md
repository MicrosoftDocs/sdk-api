---
UID: NN:mfobjects.IMFAsyncCallback
title: IMFAsyncCallback (mfobjects.h)
description: Callback interface to notify the application when an asynchronous method completes. (IMFAsyncCallback)
helpviewer_keywords: ["7edff985-da59-4cc0-96de-1a92e03a7d41","IMFAsyncCallback","IMFAsyncCallback interface [Media Foundation]","IMFAsyncCallback interface [Media Foundation]","described","mf.imfasynccallback","mfobjects/IMFAsyncCallback"]
old-location: mf\imfasynccallback.htm
tech.root: mf
ms.assetid: 7edff985-da59-4cc0-96de-1a92e03a7d41
ms.date: 12/05/2018
ms.keywords: 7edff985-da59-4cc0-96de-1a92e03a7d41, IMFAsyncCallback, IMFAsyncCallback interface [Media Foundation], IMFAsyncCallback interface [Media Foundation],described, mf.imfasynccallback, mfobjects/IMFAsyncCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAsyncCallback
 - mfobjects/IMFAsyncCallback
dev_langs:
 - c++
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
---

# IMFAsyncCallback interface


## -description

Callback interface to notify the application when an asynchronous method completes.

## -inheritance

The <b>IMFAsyncCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFAsyncCallback</b> also has these types of members:

## -remarks

For more information about asynchronous methods in Microsoft Media Foundation, see <a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>.
      

This interface is also used to perform  a work item in a Media Foundation work-queue. For more information, see <a href="/windows/desktop/medfound/work-queues">Work Queues</a>. 

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback">MFInvokeCallback</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
