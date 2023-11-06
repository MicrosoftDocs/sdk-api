---
UID: NF:subscriptionservices.IWMPSubscriptionService2.serviceEvent
title: IWMPSubscriptionService2::serviceEvent (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The serviceEvent method is called when the online store is activated or deactivated.
helpviewer_keywords: ["IWMPSubscriptionService2 interface [Windows Media Player]","serviceEvent method","IWMPSubscriptionService2.serviceEvent","IWMPSubscriptionService2::serviceEvent","IWMPSubscriptionService2serviceEvent","serviceEvent","serviceEvent method [Windows Media Player]","serviceEvent method [Windows Media Player]","IWMPSubscriptionService2 interface","subscriptionservices/IWMPSubscriptionService2::serviceEvent","wmp.iwmpsubscriptionservice2_serviceevent"]
old-location: wmp\iwmpsubscriptionservice2_serviceevent.htm
tech.root: WMP
ms.assetid: 5937cf18-2548-45da-87eb-519448e64405
ms.date: 4/26/2023
ms.keywords: IWMPSubscriptionService2 interface [Windows Media Player],serviceEvent method, IWMPSubscriptionService2.serviceEvent, IWMPSubscriptionService2::serviceEvent, IWMPSubscriptionService2serviceEvent, serviceEvent, serviceEvent method [Windows Media Player], serviceEvent method [Windows Media Player],IWMPSubscriptionService2 interface, subscriptionservices/IWMPSubscriptionService2::serviceEvent, wmp.iwmpsubscriptionservice2_serviceevent
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
 - IWMPSubscriptionService2::serviceEvent
 - subscriptionservices/IWMPSubscriptionService2::serviceEvent
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
 - IWMPSubscriptionService2.serviceEvent
---

# IWMPSubscriptionService2::serviceEvent


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>serviceEvent</b> method is called when the online store is activated or deactivated.

## -parameters

### -param event [in]

A <a href="/windows/desktop/api/subscriptionservices/ne-subscriptionservices-wmpsubscriptionserviceevent">WMPSubscriptionServiceEvent</a> enumeration value indicating whether the service is activated or deactivated.

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

Your code should not perform lengthy operations synchronously when Windows Media Player calls this method. Instead, you must perform time-consuming tasks on a separate worker thread.

## -see-also

<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2">IWMPSubscriptionService2 Interface</a>



<a href="/windows/desktop/api/subscriptionservices/ne-subscriptionservices-wmpsubscriptionserviceevent">WMPSubscriptionServiceEvent</a>