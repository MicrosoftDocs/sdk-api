---
UID: NN:mbnapi.IMbnVendorSpecificEvents
title: IMbnVendorSpecificEvents (mbnapi.h)
description: This notification interface signals an application of the completion status of vendor-specific operations and other vendor-specific changes in the device state.
old-location: mbn\imbnvendorspecificevents.htm
tech.root: mbn
ms.assetid: 28507e68-5eaa-4b9d-bbb4-e276f4c213d5
ms.date: 12/05/2018
ms.keywords: IMbnVendorSpecificEvents, IMbnVendorSpecificEvents interface [Microsoft Broadband Networks], IMbnVendorSpecificEvents interface [Microsoft Broadband Networks],described, mbn.imbnvendorspecificevents, mbnapi/IMbnVendorSpecificEvents
ms.topic: interface
f1_keywords:
- mbnapi/IMbnVendorSpecificEvents
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mbnapi.h
api_name:
- IMbnVendorSpecificEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnVendorSpecificEvents interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification interface signals an application of the completion status of vendor-specific operations and other vendor-specific changes in the device state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnVendorSpecificEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnVendorSpecificEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnVendorSpecificEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnvendorspecificevents-oneventnotification">OnEventNotification</a>
</td>
<td align="left" width="63%">
A event has occurred in the miniport driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnvendorspecificevents-onsetvendorspecificcomplete">OnSetVendorSpecificComplete</a>
</td>
<td align="left" width="63%">
A vendor-specific operation call has completed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnVendorSpecificEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnVendorSpecificEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



