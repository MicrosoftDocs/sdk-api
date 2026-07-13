---
UID: NF:mfapi.MFInvokeCallback
title: MFInvokeCallback function (mfapi.h)
description: Invokes a callback method to complete an asynchronous operation. (MFInvokeCallback)
helpviewer_keywords: ["28832d50-9b15-4eb0-96f9-2032d4edcaf4","MFInvokeCallback","MFInvokeCallback function [Media Foundation]","mf.mfinvokecallback","mfapi/MFInvokeCallback"]
old-location: mf\mfinvokecallback.htm
tech.root: mf
ms.assetid: 28832d50-9b15-4eb0-96f9-2032d4edcaf4
ms.date: 12/05/2018
ms.keywords: 28832d50-9b15-4eb0-96f9-2032d4edcaf4, MFInvokeCallback, MFInvokeCallback function [Media Foundation], mf.mfinvokecallback, mfapi/MFInvokeCallback
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFInvokeCallback
 - mfapi/MFInvokeCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFInvokeCallback
---

# MFInvokeCallback function


## -description

Invokes a callback method to complete an asynchronous operation.

## -parameters

### -param pAsyncResult

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. To create this object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult">MFCreateAsyncResult</a>.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALID_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Invalid work queue. For more information, see <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters">IMFAsyncCallback::GetParameters</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> function was called to shut down the Media Foundation platform.

</td>
</tr>
</table>

## -remarks

If you are implementing an asynchronous method, use this function to invoke the caller's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

The callback is invoked from a Media Foundation work queue. For more information, see <a href="/windows/desktop/medfound/writing-an-asynchronous-method">Writing an Asynchronous Method</a>.

The <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> function shuts down the work queue threads, so the callback is not guaranteed to be invoked after <b>MFShutdown</b> is called.

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
