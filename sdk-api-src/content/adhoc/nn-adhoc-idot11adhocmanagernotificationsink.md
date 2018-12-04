---
UID: NN:adhoc.IDot11AdHocManagerNotificationSink
title: IDot11AdHocManagerNotificationSink
author: windows-sdk-content
description: Defines the notifications supported by the IDot11AdHocManager interface.
old-location: nwifi\idot11adhocmanagernotificationsink.htm
tech.root: NativeWiFi
ms.assetid: a79931ad-deeb-4e46-a051-80a57fe5935c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDot11AdHocManagerNotificationSink, IDot11AdHocManagerNotificationSink interface [NativeWIFI], IDot11AdHocManagerNotificationSink interface [NativeWIFI],described, adhoc/IDot11AdHocManagerNotificationSink, nwifi.idot11adhocmanagernotificationsink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IDot11AdHocManagerNotificationSink interface


## -description


The <b>IDot11AdHocManagerNotificationSink</b> interface defines the notifications supported by the <a href="https://msdn.microsoft.com/dcb93b9c-3292-4cbf-9d44-5367bdbd4878">IDot11AdHocManager</a> interface. To register for notifications, call the  <a href="_com_IConnectionPoint_Advise">Advise</a> method on an instantiated <a href="https://msdn.microsoft.com/dcb93b9c-3292-4cbf-9d44-5367bdbd4878">IDot11AdHocManager</a> object with the <b>IDot11AdHocManagerNotificationSink</b> interface passed  as the <i>pUnk</i>  parameter.  To terminate notifications, call the <a href="_com_IConnectionPoint_Unadvise">Unadvise</a> method.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/A649EBBA-1076-4426-9C4D-85AB8C415C66">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocManagerNotificationSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDot11AdHocManagerNotificationSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1e2e390e-8587-4a00-9c04-b08ca026e348">IDot11AdHocManagerNotificationSink::OnInterfaceAdd</a>
</td>
<td align="left" width="63%">
Notifies the client that a new network interface card (NIC) is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac62c211-9886-4c09-8867-32ce9763c2fc">IDot11AdHocManagerNotificationSink::OnInterfaceRemove</a>
</td>
<td align="left" width="63%">
Notifies the client that a network interface card (NIC) has become inactive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28cca237-31a5-4018-a382-17d0a13a254b">IDot11AdHocManagerNotificationSink::OnNetworkAdd</a>
</td>
<td align="left" width="63%">
Notifies the client that a new wireless ad hoc network destination is in range and available for connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f325b86-3aff-4344-a154-86b74a922372">IDot11AdHocManagerNotificationSink::OnNetworkRemove</a>
</td>
<td align="left" width="63%">
Notifies the client that a wireless ad hoc network destination is no longer  available for connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dcb93b9c-3292-4cbf-9d44-5367bdbd4878">IDot11AdHocManager</a>
 

 

