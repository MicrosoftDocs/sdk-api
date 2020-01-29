---
UID: NN:mbnapi.IMbnInterfaceManager
title: IMbnInterfaceManager (mbnapi.h)
description: Provides access to IMbnInterface objects and notifications.
old-location: mbn\imbninterfacemanager.htm
tech.root: mbn
ms.assetid: a998381e-47de-4352-bc84-b6edca2f3fcc
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceManager, IMbnInterfaceManager interface [Microsoft Broadband Networks], IMbnInterfaceManager interface [Microsoft Broadband Networks],described, mbn.imbninterfacemanager, mbnapi/IMbnInterfaceManager
f1_keywords:
- mbnapi/IMbnInterfaceManager
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
- IMbnInterfaceManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterfaceManager interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Provides access to <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> objects and notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnInterfaceManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnInterfaceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnInterfaceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfacemanager-getinterface">GetInterface</a>
</td>
<td align="left" width="63%">
Gets a specific interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfacemanager-getinterfaces">GetInterfaces</a>
</td>
<td align="left" width="63%">
Gets a list of all available interfaces.

</td>
</tr>
</table> 


## -remarks



This interface can be used to access the following notification interfaces.<table>
<tr>
<th>Notification Sink to Register</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanagerevents">IMbnInterfaceManagerEvents</a>
</td>
<td><b>IID_IMbnInterfaceManagerEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>
</td>
<td><b>IID_IMbnInterfaceEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignalevents">IMbnSignalEvents</a>
</td>
<td><b>IID_IMbnSignalEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanagerevents">IMbnPinManagerEvents</a>
</td>
<td><b>IID_IMbnPinManagerEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinevents">IMbnPinEvents</a>
</td>
<td><b>IID_IMbnPinEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>
</td>
<td><b>IID_IMbnRegistrationEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontextevents">IMbnConnectionContextEvents</a>
</td>
<td><b>IID_IMbnConnectionContextEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a>
</td>
<td><b>IID_IMbnSmsEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnserviceactivationevents">IMbnServiceActivationEvents</a>
</td>
<td><b>IID_IMbnServiceActivationEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnvendorspecificevents">IMbnVendorSpecificEvents</a>
</td>
<td><b>IID_IMbnVendorSpecificEvents</b></td>
</tr>
</table>
 



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <b>IMbnInterfaceManager</b> object.</li>
<li>
For each notification sink to register, call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass IID corresponding to the notification sink to <i>riid</i>.

</li>
<li>For each connection point returned by step 2, call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements the matching notification interface to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="https://docs.microsoft.com/en-us/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points">COM Connection Points</a> article.



