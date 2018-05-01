---
UID: NN:stiusd.IStiDeviceControl
title: IStiDeviceControl
author: windows-driver-content
description: This section describes the methods defined for the IStiDeviceControl COM Interface. Method prototypes are contained in Stiusd.h.
old-location: image\istidevicecontrol_interface_methods.htm
old-project: image
ms.assetid: de58597a-d10a-45b3-bf75-539e5cd00535
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IStiDeviceControl, IStiDeviceControl interface [Imaging Devices], IStiDeviceControl interface [Imaging Devices], described, image.istidevicecontrol_interface_methods, stifnc_532906f7-46b9-4874-8099-6be551e77711.xml, stiusd/IStiDeviceControl
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
-	IStiDeviceControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiDeviceControl interface


## -description



This section describes the methods defined for the <a href="https://msdn.microsoft.com/6d98f5d7-c471-4abb-8e69-dbac3d336c2f">IStiDeviceControl COM Interface</a>. Method prototypes are contained in <i>Stiusd.h</i>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStiDeviceControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStiDeviceControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStiDeviceControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aa28efb-a030-4fed-b9f2-0e67ff1e7c9e">AddRef</a>
</td>
<td align="left" width="63%">
The <b>IStiDeviceControl::AddRef</b> method increments the reference count for the <b>IStiDeviceControl</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B20B2AE6-A408-451C-B46D-803139E8B57F">GetMyDeviceHandle</a>
</td>
<td align="left" width="63%">
This topic describes the <a href="https://msdn.microsoft.com/B20B2AE6-A408-451C-B46D-803139E8B57F">GetMyDeviceHandle</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/814e739f-6147-4287-876e-db6fc41c5aa1">GetMyDeviceOpenMode</a>
</td>
<td align="left" width="63%">
The <b>IStiDeviceControl::GetMyDeviceOpenMode</b> method allows a still image minidriver to obtain the transfer mode that an application specified when it created an instance of a still image device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f400ab05-aea9-4154-a725-5b23a6dc06b6">GetMyDevicePortName</a>
</td>
<td align="left" width="63%">
The <b>IStiDeviceControl::GetMyDevicePortName</b> method allows a user-mode still image minidriver to obtain a device's port name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56c2ddc0-9f25-4d4f-9f6e-d8c96c9acc91">Release</a>
</td>
<td align="left" width="63%">
The <b>IStiDeviceControl::Release</b> method closes the instance of the COM object that was created when a minidriver client called <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22f9688e-1e61-46a6-a9f6-0244d7dd47ce">WriteToErrorLog</a>
</td>
<td align="left" width="63%">
The <b>IStiDeviceControl::WriteToErrorLog</b> method allows a user-mode still image minidriver to write a message into the still image error log.

</td>
</tr>
</table> 

