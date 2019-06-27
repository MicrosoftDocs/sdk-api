---
UID: NN:adhoc.IDot11AdHocManagerNotificationSink
title: IDot11AdHocManagerNotificationSink (adhoc.h)
author: windows-sdk-content
description: Defines the notifications supported by the IDot11AdHocManager interface.
old-location: nwifi\idot11adhocmanagernotificationsink.htm
tech.root: NativeWiFi
ms.assetid: a79931ad-deeb-4e46-a051-80a57fe5935c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDot11AdHocManagerNotificationSink, IDot11AdHocManagerNotificationSink interface [NativeWIFI], IDot11AdHocManagerNotificationSink interface [NativeWIFI],described, adhoc/IDot11AdHocManagerNotificationSink, nwifi.idot11adhocmanagernotificationsink
ms.topic: interface
f1_keywords: 
 - "adhoc/IDot11AdHocManagerNotificationSink"
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
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
 - adhoc.h
api_name:
 - IDot11AdHocManagerNotificationSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDot11AdHocManagerNotificationSink interface


## -description


The <b>IDot11AdHocManagerNotificationSink</b> interface defines the notifications supported by the <a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a> interface. To register for notifications, call the  <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> method on an instantiated <a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a> object with the <b>IDot11AdHocManagerNotificationSink</b> interface passed  as the <i>pUnk</i>  parameter.  To terminate notifications, call the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> method.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://docs.microsoft.com/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocManagerNotificationSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDot11AdHocManagerNotificationSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDot11AdHocManagerNotificationSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanagernotificationsink-oninterfaceadd">IDot11AdHocManagerNotificationSink::OnInterfaceAdd</a>
</td>
<td align="left" width="63%">
Notifies the client that a new network interface card (NIC) is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanagernotificationsink-oninterfaceremove">IDot11AdHocManagerNotificationSink::OnInterfaceRemove</a>
</td>
<td align="left" width="63%">
Notifies the client that a network interface card (NIC) has become inactive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanagernotificationsink-onnetworkadd">IDot11AdHocManagerNotificationSink::OnNetworkAdd</a>
</td>
<td align="left" width="63%">
Notifies the client that a new wireless ad hoc network destination is in range and available for connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanagernotificationsink-onnetworkremove">IDot11AdHocManagerNotificationSink::OnNetworkRemove</a>
</td>
<td align="left" width="63%">
Notifies the client that a wireless ad hoc network destination is no longer  available for connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a>
 

 

