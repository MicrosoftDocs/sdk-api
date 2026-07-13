---
UID: NF:subscriptionservices.IWMPSubscriptionService2.prepareForSync
title: IWMPSubscriptionService2::prepareForSync (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionService2 interface [Windows Media Player]","prepareForSync method","IWMPSubscriptionService2.prepareForSync","IWMPSubscriptionService2::prepareForSync","IWMPSubscriptionService2prepareForSync","prepareForSync","prepareForSync method [Windows Media Player]","prepareForSync method [Windows Media Player]","IWMPSubscriptionService2 interface","subscriptionservices/IWMPSubscriptionService2::prepareForSync","wmp.iwmpsubscriptionservice2_prepareforsync"]
old-location: wmp\iwmpsubscriptionservice2_prepareforsync.htm
tech.root: WMP
ms.assetid: 64ab5548-b562-44e4-9798-8f14d3ed653b
ms.date: 4/26/2023
ms.keywords: IWMPSubscriptionService2 interface [Windows Media Player],prepareForSync method, IWMPSubscriptionService2.prepareForSync, IWMPSubscriptionService2::prepareForSync, IWMPSubscriptionService2prepareForSync, prepareForSync, prepareForSync method [Windows Media Player], prepareForSync method [Windows Media Player],IWMPSubscriptionService2 interface, subscriptionservices/IWMPSubscriptionService2::prepareForSync, wmp.iwmpsubscriptionservice2_prepareforsync
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
 - IWMPSubscriptionService2::prepareForSync
 - subscriptionservices/IWMPSubscriptionService2::prepareForSync
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
 - IWMPSubscriptionService2.prepareForSync
---

# IWMPSubscriptionService2::prepareForSync


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>prepareForSync</b> method is implemented by the online store and called by Windows Media Player just before synchronization happens. Use this method to perform tasks related to synchronizing a digital media file to a device.

## -parameters

### -param bstrFilename [in]

String containing the name of the digital media file being synchronized.

### -param bstrDeviceName [in]

String containing the canonical name of the device.

### -param pCB [in]

Pointer to an <a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback">IWMPSubscriptionServiceCallback</a> interface. The online store uses this pointer to notify Windows Media Player that preparation for synchronization is complete.

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

The string contained in <i>bstrDeviceName</i> is not the same name retrieved using <a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_devicename">IWMPSyncDevice::get_deviceName</a>. Rather, it is the canonical name retrieved by using the <b>IWMDMDevice2::GetCanonicalName</b> method provided by the Windows Media Device Manager SDK.

Your code should not perform lengthy operations synchronously when Windows Media Player calls this method. Instead, you must perform time-consuming tasks on a separate worker thread. When the worker thread has completed its work, it must call <a href="/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete">IWMPSubscriptionServiceCallback::onComplete</a>.

Use the following procedure to provide your worker thread with a pointer to an <b>IWMPSubscriptionServiceCallback</b> interface.

<ol>
<li>Pass <i>pCB</i> to <b>CoMarshalInterThreadInterfaceInStream</b>, which returns an <b>IStream</b> pointer.</li>
<li>Pass the <b>IStream</b> pointer to your worker thread.</li>
<li>In your worker thread, call <b>CoGetInterfaceAndReleaseStream</b>, which returns an interface pointer that you can use to call <b>onComplete</b>.</li>
</ol>
When you call <a href="/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete">IWMPSubscriptionServiceCallback::onComplete</a>, you should return a success code to allow Windows Media Player to continue synchronizing the specified digital media file, or an error code to disallow synchronization. Windows Media Player displays an error message based on the error code you provide. You should avoid using generic <b>HRESULTs</b>, such as E_FAIL. Instead, you can return the <b>HRESULT</b> error code you receive from a call to one of the Windows Media SDKs, such as the Windows Media Device Manager SDK, or one of the error codes in nserror.h, which can be found in the \Include folder where you installed the Windows Media Player SDK.

## -see-also

<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2">IWMPSubscriptionService2 Interface</a>



<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback">IWMPSubscriptionServiceCallback Interface</a>