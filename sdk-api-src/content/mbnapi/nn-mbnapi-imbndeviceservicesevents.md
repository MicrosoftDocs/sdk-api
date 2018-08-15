---
UID: NN:mbnapi.IMbnDeviceServicesEvents
title: IMbnDeviceServicesEvents
author: windows-sdk-content
description: Signals an application about notification events related to Mobile Broadband device services on the system.
old-location: mbn\imbndeviceservicesevents.htm
old-project: mbn
ms.assetid: 66A388D0-C704-45D2-AD56-4F81E1928774
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnDeviceServicesEvents, IMbnDeviceServicesEvents interface [Microsoft Broadband Networks], IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],described, mbn.imbndeviceservicesevents, mbnapi/IMbnDeviceServicesEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceServicesEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceServicesEvents interface


## -description


Signals an application about notification events related to Mobile Broadband device services on the system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceServicesEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnDeviceServicesEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnDeviceServicesEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DD313EF9-E45A-418E-91D5-0BD16C42972A">OnCloseCommandSessionComplete</a>
</td>
<td align="left" width="63%">
Notification method indicating that a device service <b>CloseCommandSession</b> request has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/003D87F7-CFFD-47A3-8DAA-0CF9F64E2CF6">OnCloseDataSessionComplete</a>
</td>
<td align="left" width="63%">
Notification method indicating that a device service session <b>CloseDataSession</b> request has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6C3B223A-E791-4861-B93B-1EDC0DC8038B">OnEventNotification</a>
</td>
<td align="left" width="63%">
Notification method signaling a device service state change event from the Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6677E80E-A9D1-45B5-AE3F-71EE22A7CCB6">OnInterfaceStateChange</a>
</td>
<td align="left" width="63%">
Notification method that signals a change in the state of device services on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DE8F8AB7-62DE-47B1-A8E2-E24DFC63892E">OnOpenCommandSessionComplete</a>
</td>
<td align="left" width="63%">
Notification method indicating that a device service <b>CommandSessionOpen</b> request has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50FDF285-0C93-45C3-AB07-9BFB067DAD94">OnOpenDataSessionComplete</a>
</td>
<td align="left" width="63%">
Notification method indicating that a device service <b>OpenDataSession</b> request has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6A04FA3F-D5E4-4E02-A334-218A168762AB">OnQueryCommandComplete</a>
</td>
<td align="left" width="63%">
Notification method indicating that a device service <b>QUERY</b> request has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CA304FF5-B630-4CD5-8E23-844499D6A8D1">OnQuerySupportedCommandsComplete</a>
</td>
<td align="left" width="63%">
Notification method indicating that a query for the messages supported on a device service has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14D2A2A3-E3E0-4C8B-B4FE-F85CA1316877">OnReadData</a>
</td>
<td align="left" width="63%">
Notification for data being read from a device service data session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A388F548-453B-4DAB-8AD8-ABC26B22F20E">OnSetCommandComplete</a>
</td>
<td align="left" width="63%">
Notification method indicating that a device service <b>SET</b> request has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2C885E15-C689-4ADF-BFB0-24D03932FAC7">OnWriteDataComplete</a>
</td>
<td align="left" width="63%">
Notification method indicating that a device service session <b>Write</b> request has completed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.<ol>
<li>Get an <a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a> interface by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on an <a href="https://msdn.microsoft.com/6CFF2275-0649-4009-84F2-0657B2FF281C">IMbnDeviceServicesManager</a> object.</li>
<li>Call <a href="https://msdn.microsoft.com/bbe55013-13ca-43e8-8d5e-ef89076df039">FindConnectionPoint</a> on the returned interface and pass IID_IMbnDeviceServicesEvents to RIID.</li>
<li>Call <a href="https://msdn.microsoft.com/11257f24-096c-4240-8fac-4e42a6161d66">Advise</a> on the returned connection point and pass a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on an object that implements <b>IMbnDeviceServicesEvents</b> to PUNK.</li>
</ol>


Notifications can be terminated by calling <a href="https://msdn.microsoft.com/71641bad-2fd1-4d94-a6d0-116f5687a95b">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://msdn.microsoft.com/en-us/magazine/cc163361.aspx">COM Connection Points article</a>.



