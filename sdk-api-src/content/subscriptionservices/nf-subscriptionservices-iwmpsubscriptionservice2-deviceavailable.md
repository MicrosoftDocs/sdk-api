---
UID: NF:subscriptionservices.IWMPSubscriptionService2.deviceAvailable
title: IWMPSubscriptionService2::deviceAvailable (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionService2 interface [Windows Media Player]","deviceAvailable method","IWMPSubscriptionService2.deviceAvailable","IWMPSubscriptionService2::deviceAvailable","IWMPSubscriptionService2doMetering","deviceAvailable","deviceAvailable method [Windows Media Player]","deviceAvailable method [Windows Media Player]","IWMPSubscriptionService2 interface","subscriptionservices/IWMPSubscriptionService2::deviceAvailable","wmp.iwmpsubscriptionservice2_deviceavailable"]
old-location: wmp\iwmpsubscriptionservice2_deviceavailable.htm
tech.root: WMP
ms.assetid: f3450e57-5e25-411c-8b21-b687021a6500
ms.date: 4/26/2023
ms.keywords: IWMPSubscriptionService2 interface [Windows Media Player],deviceAvailable method, IWMPSubscriptionService2.deviceAvailable, IWMPSubscriptionService2::deviceAvailable, IWMPSubscriptionService2doMetering, deviceAvailable, deviceAvailable method [Windows Media Player], deviceAvailable method [Windows Media Player],IWMPSubscriptionService2 interface, subscriptionservices/IWMPSubscriptionService2::deviceAvailable, wmp.iwmpsubscriptionservice2_deviceavailable
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
 - IWMPSubscriptionService2::deviceAvailable
 - subscriptionservices/IWMPSubscriptionService2::deviceAvailable
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
 - IWMPSubscriptionService2.deviceAvailable
---

# IWMPSubscriptionService2::deviceAvailable


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>deviceAvailable</b> method is implemented by the online store to initiate device-specific processing tasks.

## -parameters

### -param bstrDeviceName [in]

String containing the device name.

### -param pCB [in]

Pointer to an <b>IWMPSubscriptionServiceCallback</b> interface. The online store uses this pointer to notify Windows Media Player that device-specific processing is complete.

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

Windows Media Player calls this method after a synchronization operation if the time elapsed since the last call is one week or more.

Your code should not perform lengthy operations synchronously when Windows Media Player calls this method. Instead, you must perform time-consuming tasks on a separate worker thread. When the worker thread has completed its work, it must call <a href="/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete">IWMPSubscriptionServiceCallback::onComplete</a>.

Use the following procedure to provide your worker thread with a pointer to an <b>IWMPSubscriptionServiceCallback</b> interface.

<ol>
<li>Pass <i>pCB</i> to <b>CoMarshalInterThreadInterfaceInStream</b>, which returns an <b>IStream</b> pointer.</li>
<li>Pass the <b>IStream</b> pointer to your worker thread.</li>
<li>In your worker thread, call <b>CoGetInterfaceAndReleaseStream</b>, which returns an interface pointer that you can use to call <b>onComplete</b>.</li>
</ol>
The string contained in <i>bstrDeviceName</i> is not the same name retrieved by using <a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_devicename">IWMPSyncDevice::get_deviceName</a>. Rather, it is the canonical name retrieved by using the <b>IWMDMDevice2::GetCanonicalName</b> method provided by the Windows Media Device Manager SDK.

## -see-also

<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2">IWMPSubscriptionService2 Interface</a>



<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback">IWMPSubscriptionServiceCallback Interface</a>