---
UID: NN:wcndevice.IWCNDevice
title: IWCNDevice
author: windows-sdk-content
description: Use this interface to configure the device and initiate the session.
old-location: wcn\iwcndevice.htm
old-project: wcn
ms.assetid: a092406d-7af4-436d-9755-5a9b87aa6ca9
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWCNDevice, IWCNDevice interface [Windows Connect Now], IWCNDevice interface [Windows Connect Now],described, wcn.iwcndevice, wcndevice/IWCNDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WCN_SESSION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WcnDevice.h
api_name:
-	IWCNDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWCNDevice interface


## -description


Use this interface to configure the device and initiate the session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWCNDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWCNDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWCNDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">Connect</a>
</td>
<td align="left" width="63%">
Initiates the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06a73bb5-c339-4069-853d-ab22c15c1462">GetAttribute</a>
</td>
<td align="left" width="63%">
Gets a cached attribute  from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95ad3427-c8c9-4ac9-8c8e-c9bedf855a37">GetIntegerAttribute</a>
</td>
<td align="left" width="63%">
Gets a cached attribute  from the device as an integer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4fb0fc3-a45e-444c-953a-fe4fdfb0b327">GetNetworkProfile</a>
</td>
<td align="left" width="63%">
Gets a network profile from the device.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ef065be-0046-4ce6-8f81-417a4c8a550a">GetStringAttribute</a>
</td>
<td align="left" width="63%">
Gets a cached attribute from the device as a string.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7fa8446-8013-431a-95ed-fa5d78a90df7">GetVendorExtension</a>
</td>
<td align="left" width="63%">
Gets a cached vendor extension from the device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/267aa55a-005d-4db8-9569-f8ee77a15168">SetNetworkProfile</a>
</td>
<td align="left" width="63%">
Queues an XML WLAN profile to be provisioned to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">SetPassword</a>
</td>
<td align="left" width="63%">
Configures the authentication method value, and if required, a password used for the pending session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed96b9bc-4f4e-48bb-9c1d-8a0ababe0b26">SetVendorExtension</a>
</td>
<td align="left" width="63%">
Queues a vendor extension for use in the pending session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d76ebc9e-8adc-4640-a377-f69cef43afca">Unadvise</a>
</td>
<td align="left" width="63%">
Removes any callback previously set via <a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/63ea2b5a-4bec-4050-9a61-962a1faef0a0">IWCNConnectNotify</a>
 

 

