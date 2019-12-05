---
UID: NN:adhoc.IDot11AdHocManager
title: IDot11AdHocManager (adhoc.h)
description: Creates and manages 802.11 ad hoc networks.
old-location: nwifi\idot11adhocmanager.htm
tech.root: NativeWiFi
ms.assetid: dcb93b9c-3292-4cbf-9d44-5367bdbd4878
ms.date: 12/05/2018
ms.keywords: IDot11AdHocManager, IDot11AdHocManager interface [NativeWIFI], IDot11AdHocManager interface [NativeWIFI],described, adhoc/IDot11AdHocManager, nwifi.idot11adhocmanager
ms.topic: interface
f1_keywords:
- adhoc/IDot11AdHocManager
dev_langs:
- c++
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
- IDot11AdHocManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDot11AdHocManager interface


## -description


The <b>IDot11AdHocManager</b> interface creates and manages 802.11 ad hoc networks.  It is the top-level 802.11 ad hoc interface and the only ad hoc interface with a coclass. As such, it is the only ad hoc interface that can be instantiated by <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. 
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://docs.microsoft.com/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>The <b>IDot11AdHocManager</b> coclass implements the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface. The <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> method can be used to register for network manager, network, and interface-related notifications. Notifications are implemented by the <a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink">IDot11AdHocManagerNotificationSink</a> interface. To register for notifications, call the <b>Advise</b> method with the appropriate notification sink interface as the <i>pUnk</i>  parameter.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDot11AdHocManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDot11AdHocManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-commitcreatednetwork">IDot11AdHocManager::CommitCreatedNetwork</a>
</td>
<td align="left" width="63%">
Initializes a created network and optionally commits the network's profile to the profile store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-createnetwork">IDot11AdHocManager::CreateNetwork</a>
</td>
<td align="left" width="63%">
Creates a wireless ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-getienumdot11adhocinterfaces">IDot11AdHocManager::GetIEnumDot11AdHocInterfaces</a>
</td>
<td align="left" width="63%">
Returns the set of wireless network interface cards (NICs) available on the machine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-getienumdot11adhocnetworks">IDot11AdHocManager::GetIEnumDot11AdHocNetworks</a>
</td>
<td align="left" width="63%">
Returns a list of available ad hoc network destinations within connection range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-getnetwork">IDot11AdHocManager::GetNetwork</a>
</td>
<td align="left" width="63%">
Returns the network associated with a signature. 

</td>
</tr>
</table> 

