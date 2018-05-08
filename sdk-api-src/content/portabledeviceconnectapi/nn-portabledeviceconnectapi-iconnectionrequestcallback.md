---
UID: NN:portabledeviceconnectapi.IConnectionRequestCallback
title: IConnectionRequestCallback
author: windows-driver-content
description: Defines a single callback method.
old-location: wpdsdk\iconnectionrequestcallback.htm
old-project: wpd_sdk
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IConnectionRequestCallback, IConnectionRequestCallback interface [Windows Portable Devices SDK], IConnectionRequestCallback interface [Windows Portable Devices SDK],described, devpkey/IConnectionRequestCallback, portabledeviceconnectapi/IConnectionRequestCallback, wpdsdk.iconnectionrequestcallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: portabledeviceconnectapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceconnectapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGuids.lib
-	PortableDeviceGuids.dll
api_name:
-	IConnectionRequestCallback
product: Windows
targetos: Windows
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IConnectionRequestCallback interface


## -description


The <b>IConnectionRequestCallback</b> interface defines a single callback method. A Windows Portable Devices (WPD) application implements this optional Component Object Model (COM) interface to receive notifications about completed requests and to cancel pending requests. The requests are sent using the<a href="https://msdn.microsoft.com/2bb5b124-3018-4619-bb8f-67fcfc8981d9"> IPortableDeviceConnector::Connect</a> and <a href="https://msdn.microsoft.com/0cc104e6-5e3a-4fce-ba3b-68f3fb94196b">IPortableDeviceConnector::Disconnect</a> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectionRequestCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConnectionRequestCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConnectionRequestCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665">OnComplete</a>
</td>
<td align="left" width="63%">
Notifies an application that a previously scheduled request has completed.

</td>
</tr>
</table> 

