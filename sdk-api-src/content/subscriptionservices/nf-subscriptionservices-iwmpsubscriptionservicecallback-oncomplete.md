---
UID: NF:subscriptionservices.IWMPSubscriptionServiceCallback.onComplete
title: IWMPSubscriptionServiceCallback::onComplete (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The onComplete method notifies Windows Media Player when a background process is completed.
helpviewer_keywords: ["IWMPSubscriptionServiceCallback interface [Windows Media Player]","onComplete method","IWMPSubscriptionServiceCallback.onComplete","IWMPSubscriptionServiceCallback::onComplete","IWMPSubscriptionServiceCallbackonComplete","onComplete","onComplete method [Windows Media Player]","onComplete method [Windows Media Player]","IWMPSubscriptionServiceCallback interface","subscriptionservices/IWMPSubscriptionServiceCallback::onComplete","wmp.iwmpsubscriptionservicecallback_oncomplete"]
old-location: wmp\iwmpsubscriptionservicecallback_oncomplete.htm
tech.root: WMP
ms.assetid: 1a6775b5-a909-49b1-98e8-ccc110294df6
ms.date: 4/26/2023
ms.keywords: IWMPSubscriptionServiceCallback interface [Windows Media Player],onComplete method, IWMPSubscriptionServiceCallback.onComplete, IWMPSubscriptionServiceCallback::onComplete, IWMPSubscriptionServiceCallbackonComplete, onComplete, onComplete method [Windows Media Player], onComplete method [Windows Media Player],IWMPSubscriptionServiceCallback interface, subscriptionservices/IWMPSubscriptionServiceCallback::onComplete, wmp.iwmpsubscriptionservicecallback_oncomplete
req.header: subscriptionservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSubscriptionServiceCallback::onComplete
 - subscriptionservices/IWMPSubscriptionServiceCallback::onComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - subscriptionservices.h
api_name:
 - IWMPSubscriptionServiceCallback.onComplete
---

# IWMPSubscriptionServiceCallback::onComplete


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>onComplete</b> method notifies Windows Media Player when a background process is completed.

## -parameters

### -param hrResult [in]

<b>HRESULT</b> success or error code.

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

<a href="/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync">IWMPSubscriptionService2::prepareForSync</a> and <a href="/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable">IWMPSubscriptionService2::deviceAvailable</a> supply a pointer to an <b>IWMPSubscriptionServiceCallback</b> interface. When responding to calls from Windows Media Player to these methods, you must pass any time-consuming tasks to a separate worker thread and return immediately. When the worker thread has completed its task, it must call <b>IWMPSubscriptionServiceCallback::onComplete</b>.

In your <b>prepareForSync</b> and <b>deviceAvailable</b> methods, use the following procedure to provide your worker thread with a pointer to an <b>IWMPSubscriptionServiceCallback</b> interface.

<ol>
<li>Pass the pointer supplied in the <i>pCB</i> parameter to <b>CoMarshalInterThreadInterfaceInStream</b>, which returns an <b>IStream</b> pointer.</li>
<li>Pass the <b>IStream</b> pointer to your worker thread.</li>
<li>In your worker thread, call <b>CoGetInterfaceAndReleaseStream</b>, which returns an interface pointer that you can use to call <b>onComplete</b>.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback">IWMPSubscriptionServiceCallback Interface</a>