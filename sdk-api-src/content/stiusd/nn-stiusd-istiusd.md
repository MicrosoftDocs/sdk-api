---
UID: NN:stiusd.IStiUSD
title: IStiUSD
author: windows-driver-content
description: This section describes the methods defined for the IStiUSD COM Interface. Method prototypes are contained in Stiusd.h.
old-location: image\istiusd_interface_methods.htm
old-project: image
ms.assetid: 62740263-5bbb-48e1-be3d-9ee9cb37d6b9
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IStiUSD, IStiUSD interface [Imaging Devices], IStiUSD interface [Imaging Devices], described, image.istiusd_interface_methods, stifnc_2fa7c229-f4c5-455e-ba93-019c5b84dd79.xml, stiusd/IStiUSD
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: stiusd.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	stiusd.h
api_name:
-	IStiUSD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiUSD interface


## -description



This section describes the methods defined for the <a href="https://msdn.microsoft.com/2f805955-8c66-4c9e-839e-c8a98c6637a8">IStiUSD COM Interface</a>. Method prototypes are contained in <i>Stiusd.h</i>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStiUSD</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStiUSD</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStiUSD</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn939354">DeviceReset</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::DeviceReset</b> method resets a still image device to a known, initialized state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf99c34e-5a71-4f2b-8dca-bed87d18b352">Diagnostic</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::Diagnostic</b> method runs diagnostic tests on a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt637428">Escape</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::Escape</b> method performs a vendor-specific I/O operation on a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451391">GetCapabilities</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::GetCapabilities</b> method returns a still image device's capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7f265b8-c8a9-4a79-85e2-e3f52bf25f31">GetLastError</a>
</td>
<td align="left" width="63%">
The <b>IStiUSD::GetLastError</b> method returns the last known error associated with a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b393f55-6054-4c45-aa3d-7588139b34e5">GetLastErrorInfo</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::GetLastErrorInfo</b> method returns information about the last known error associated with a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4293fa8-07c9-40b2-acc2-8a3128b6dad4">GetNotificationData</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::GetNotificationData</b> method returns a description of the most recent event that occurred on a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::GetStatus</b> method returns the status of a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::Initialize</b> method initializes an instance of the COM object that defines the <b>IStiUSD</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb91ef14-53d7-42fa-b3e5-54eb3b0925b8">LockDevice</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::LockDevice</b> method locks a device for exclusive use by the caller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/603f8b76-eb3b-41aa-932c-322f5405a29b">RawReadCommand</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::RawReadCommand</b> method reads command information from a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ae64309-da53-420b-bf87-e8924e902dba">RawReadData</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::RawReadData</b> method reads data from a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1b03ff5-1924-4221-b177-15214a8bf4f1">RawWriteCommand</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiDevice::RawWriteCommand</b> method sends command information to a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82700669-b98f-486c-a7a6-cd7138300f11">RawWriteData</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::RawWriteData</b> method writes data to a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/096e9b7a-fc50-46a2-b67a-7128dba13321">SetNotificationHandle</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::SetNotificationHandle</b> method specifies an event handle that the minidriver should use to inform the caller of device events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae19ae38-3bca-42c8-8713-68bb161104b8">UnLockDevice</a>
</td>
<td align="left" width="63%">
A still image minidriver's <b>IStiUSD::UnLockDevice</b> method unlocks a device that was locked by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff543829">IStiUSD::LockDevice</a>.

</td>
</tr>
</table> 

