---
UID: NF:mfobjects.IMFAsyncCallback.Invoke
title: IMFAsyncCallback::Invoke (mfobjects.h)
description: Called when an asynchronous operation is completed. (IMFAsyncCallback.Invoke)
helpviewer_keywords: ["22473605-637e-4783-a8cb-98248b0a0327","IMFAsyncCallback interface [Media Foundation]","Invoke method","IMFAsyncCallback.Invoke","IMFAsyncCallback::Invoke","Invoke","Invoke method [Media Foundation]","Invoke method [Media Foundation]","IMFAsyncCallback interface","mf.imfasynccallback_invoke","mfobjects/IMFAsyncCallback::Invoke"]
old-location: mf\imfasynccallback_invoke.htm
tech.root: mf
ms.assetid: 22473605-637e-4783-a8cb-98248b0a0327
ms.date: 12/05/2018
ms.keywords: 22473605-637e-4783-a8cb-98248b0a0327, IMFAsyncCallback interface [Media Foundation],Invoke method, IMFAsyncCallback.Invoke, IMFAsyncCallback::Invoke, Invoke, Invoke method [Media Foundation], Invoke method [Media Foundation],IMFAsyncCallback interface, mf.imfasynccallback_invoke, mfobjects/IMFAsyncCallback::Invoke
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
 - IMFAsyncCallback::Invoke
 - mfobjects/IMFAsyncCallback::Invoke
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
 - IMFAsyncCallback.Invoke
---

# IMFAsyncCallback::Invoke


## -description

Called when an asynchronous operation is completed.

## -parameters

### -param pAsyncResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass this pointer to the asynchronous <b>End...</b> method to complete the asynchronous call.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

Within your implementation of <b>Invoke</b>, call the corresponding <b>End...</b> method.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback">MFInvokeCallback</a>
