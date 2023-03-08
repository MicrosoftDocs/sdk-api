---
UID: NN:mfobjects.IMFAsyncResult
title: IMFAsyncResult (mfobjects.h)
description: Provides information about the result of an asynchronous operation. (IMFAsyncResult)
helpviewer_keywords: ["8c95b1de-8974-445c-8070-41552ea83e53","IMFAsyncResult","IMFAsyncResult interface [Media Foundation]","IMFAsyncResult interface [Media Foundation]","described","mf.imfasyncresult","mfobjects/IMFAsyncResult"]
old-location: mf\imfasyncresult.htm
tech.root: mf
ms.assetid: 8c95b1de-8974-445c-8070-41552ea83e53
ms.date: 12/05/2018
ms.keywords: 8c95b1de-8974-445c-8070-41552ea83e53, IMFAsyncResult, IMFAsyncResult interface [Media Foundation], IMFAsyncResult interface [Media Foundation],described, mf.imfasyncresult, mfobjects/IMFAsyncResult
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
 - IMFAsyncResult
 - mfobjects/IMFAsyncResult
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
 - IMFAsyncResult
---

# IMFAsyncResult interface


## -description

Provides information about the result of an asynchronous operation.

## -inheritance

The <b>IMFAsyncResult</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFAsyncResult</b> also has these types of members:

## -remarks

Use this interface to complete an asynchronous operation. You get a pointer to this interface when your callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. To complete the operation, pass the <b>IMFAsyncResult</b> pointer to the <b>End...</b> method that corresponds to the <b>Begin...</b> method that starts the operation. For example, if the asynchronous method is named <b>BeginRead</b>, call the <b>EndRead</b> method. For more information, see <a href="/windows/desktop/medfound/calling-asynchronous-methods">Calling Asynchronous Methods</a>.

If you are implementing an asynchronous method, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult">MFCreateAsyncResult</a> to create an instance of this object. For more information, see <a href="/windows/desktop/medfound/writing-an-asynchronous-method">Writing an Asynchronous Method</a>.

Any custom implementation of this interface must inherit the <a href="/windows/desktop/api/mfapi/ns-mfapi-mfasyncresult">MFASYNCRESULT</a> structure.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
