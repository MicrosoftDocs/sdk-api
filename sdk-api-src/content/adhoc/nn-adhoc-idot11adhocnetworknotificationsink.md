---
UID: NN:adhoc.IDot11AdHocNetworkNotificationSink
title: IDot11AdHocNetworkNotificationSink
author: windows-sdk-content
description: Defines the notifications supported by the IDot11AdHocNetwork interface.
old-location: nwifi\idot11adhocnetworknotificationsink.htm
tech.root: NativeWiFi
ms.assetid: 54a45431-8036-4a3f-9558-467a1efab6bb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDot11AdHocNetworkNotificationSink, IDot11AdHocNetworkNotificationSink interface [NativeWIFI], IDot11AdHocNetworkNotificationSink interface [NativeWIFI],described, adhoc/IDot11AdHocNetworkNotificationSink, nwifi.idot11adhocnetworknotificationsink
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
 - IDot11AdHocNetworkNotificationSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDot11AdHocNetworkNotificationSink interface


## -description


The <b>IDot11AdHocNetworkNotificationSink</b> interface defines the notifications supported by the <a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a> interface. To register for notifications, call the  <a href="https://msdn.microsoft.com/en-us/library/ms678815(v=VS.85).aspx">Advise</a> method on an instantiated <a href="https://msdn.microsoft.com/dcb93b9c-3292-4cbf-9d44-5367bdbd4878">IDot11AdHocManager</a> object with the <b>IDot11AdHocNetworkNotificationSink</b> interface passed  as the <i>pUnk</i>  parameter.  To terminate notifications, call the <a href="https://msdn.microsoft.com/en-us/library/ms686608(v=VS.85).aspx">Unadvise</a> method.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/A649EBBA-1076-4426-9C4D-85AB8C415C66">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocNetworkNotificationSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDot11AdHocNetworkNotificationSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDot11AdHocNetworkNotificationSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b38143c8-4e90-4f5d-b9f5-15bd1fd7e1c5">IDot11AdHocNetworkNotificationSink::OnConnectFail</a>
</td>
<td align="left" width="63%">
Notifies the client that a connection attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/795057bf-d97e-40b8-b242-5e3859ad3038">IDot11AdHocNetworkNotificationSink::OnStatusChange</a>
</td>
<td align="left" width="63%">
Notifies the client that the connection status of the network has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a>
 

 

