---
UID: NN:adhoc.IDot11AdHocInterfaceNotificationSink
title: IDot11AdHocInterfaceNotificationSink
author: windows-sdk-content
description: Defines the notifications supported by IDot11AdHocInterface.
old-location: nwifi\idot11adhocinterfacenotificationsink.htm
old-project: nativewifi
ms.assetid: ab3fd026-32b4-48cb-aa10-37a084b5b08e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDot11AdHocInterfaceNotificationSink, IDot11AdHocInterfaceNotificationSink interface [NativeWIFI], IDot11AdHocInterfaceNotificationSink interface [NativeWIFI],described, adhoc/IDot11AdHocInterfaceNotificationSink, nwifi.idot11adhocinterfacenotificationsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: adhoc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocInterfaceNotificationSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocInterfaceNotificationSink interface


## -description


The <b>IDot11AdHocInterfaceNotificationSink</b> interface defines the notifications supported by <a href="https://msdn.microsoft.com/a4a73ff8-e24a-4f44-9205-c60699d1c27d">IDot11AdHocInterface</a>. To register for notifications, call the  <a href="_com_IConnectionPoint_Advise">Advise</a> method on an instantiated <a href="https://msdn.microsoft.com/dcb93b9c-3292-4cbf-9d44-5367bdbd4878">IDot11AdHocManager</a> object with the <b>IDot11AdHocInterfaceNotificationSink</b> interface passed  as the <i>pUnk</i>  parameter.  To terminate notifications, call the <a href="_com_IConnectionPoint_Unadvise">Unadvise</a> method.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/A649EBBA-1076-4426-9C4D-85AB8C415C66">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocInterfaceNotificationSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDot11AdHocInterfaceNotificationSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDot11AdHocInterfaceNotificationSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2116e44-e29b-4110-8794-ed161fdb534d">IDot11AdHocInterfaceNotificationSink::OnConnectionStatusChange</a>
</td>
<td align="left" width="63%">
Notifies the client that the connection status of the network associated with the NIC has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a4a73ff8-e24a-4f44-9205-c60699d1c27d">IDot11AdHocInterface</a>
 

 

